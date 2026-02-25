# Social-shop
social-shop/
├── frontend/          (Next.js + React)
├── backend/           (Node.js + Express)
├── shared/            (código compartilhado)
├── .gitignore
├── README.md
└── GitHub Actions     (CI/CD configurado)
import React from 'react';
import { Navbar, Nav, Form, FormControl, Button } from 'react-bootstrap';
import { FaUserCircle, FaShoppingCart } from 'react-icons/fa';

const Header = () => {
    return (
        <Navbar bg="light" expand="lg">
            <Navbar.Brand href="#"><img src="/logo.png" alt="Logo" style={{ width: '50px' }} /></Navbar.Brand>
            <Navbar.Toggle aria-controls="basic-navbar-nav" />
            <Navbar.Collapse id="basic-navbar-nav">
                <Nav className="mr-auto">
                    <Nav.Link href="#home">Home</Nav.Link>
                    <Nav.Link href="#features">Features</Nav.Link>
                    <Nav.Link href="#pricing">Pricing</Nav.Link>
                </Nav>
                <Form inline>
                    <FormControl type="text" placeholder="Search" className="mr-sm-2" />
                    <Button variant="outline-success">Search</Button>
                </Form>
                <Nav className="ml-auto">
                    <Nav.Link href="#profile"><FaUserCircle size={24} /></Nav.Link>
                    <Nav.Link href="#cart"><FaShoppingCart size={24} /></Nav.Link>
                </Nav>
            </Navbar.Collapse>
        </Navbar>
    );
};

export default Header;import '../styles/globals.css';

function MyApp({ Component, pageProps }) {
  return <Component {...pageProps} />;
}

export default MyApp;
