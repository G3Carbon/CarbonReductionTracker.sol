// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract CarbonReductionTracker {

    address public admin;

    struct Company {
        string name;
        uint256 emissionsReduced; // Toneladas de CO2 reducidas
        uint256 rewardPoints;     // Puntos obtenidos
        bool registered;
    }

    mapping(address => Company) public companies;

    event CompanyRegistered(address company, string name);
    event ReductionRecorded(address company, uint256 tons, uint256 points);

    constructor() {
        admin = msg.sender;
    }

    modifier onlyAdmin() {
        require(msg.sender == admin, "Solo el administrador puede realizar esta accion");
        _;
    }

    function registerCompany(address _company, string memory _name) public onlyAdmin {
        require(!companies[_company].registered, "La empresa ya esta registrada");

        companies[_company] = Company({
            name: _name,
            emissionsReduced: 0,
            rewardPoints: 0,
            registered: true
        });

        emit CompanyRegistered(_company, _name);
    }

    function recordReduction(address _company, uint256 _tons) public onlyAdmin {
        require(companies[_company].registered, "Empresa no registrada");

        companies[_company].emissionsReduced += _tons;
        companies[_company].rewardPoints += (_tons * 100);

        emit ReductionRecorded(_company, _tons, _tons * 100);
    }

    function getCompany(address _company)
        public
        view
        returns (
            string memory,
            uint256,
            uint256
        )
    {
        Company memory c = companies[_company];

        return (
            c.name,
            c.emissionsReduced,
            c.rewardPoints
        );
    }
}
