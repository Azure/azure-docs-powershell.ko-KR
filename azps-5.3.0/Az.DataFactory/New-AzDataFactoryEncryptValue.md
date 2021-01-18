---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5BF24BC2-DEB6-4830-BDEA-841BAB070388
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryencryptvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
ms.openlocfilehash: 0e69cfe7ae76be1d79bdd8cf0d7db193a05219d5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493540"
---
# New-AzDataFactoryEncryptValue

## SYNOPSIS
중요한 데이터를 암호화합니다.

## 구문

### ByFactoryName(기본값)
```
New-AzDataFactoryEncryptValue [-DataFactoryName] <String> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
New-AzDataFactoryEncryptValue [-DataFactory] <PSDataFactory> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**New-AzDataFactoryEncryptValue** cmdlet은 암호 또는 Microsoft SQL Server 연결 문자열과 같은 중요한 데이터를 암호화하고 암호화된 값을 반환합니다.

## 예제

### 예제 1: 비 ODBC 연결 문자열 암호화
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

첫 번째 명령은 ConvertTo-SecureString cmdlet을 사용하여 지정된 연결 문자열을 **SecureString** 개체로 변환한 다음 해당 개체를 $Value 변수에 저장합니다.
자세한 내용은 `Get-Help ConvertTo-SecureString` .를 입력합니다.
허용되는 값: SQL Server 또는 Oracle 연결 문자열입니다.
두 번째 명령은 지정된 데이터 팩터리, 게이트웨이$Value 리소스 그룹 및 연결된 서비스 유형에 대해 $Value 개체에 대해 암호화된 값을 만듭니다.

### 예제 2: Windows 인증을 사용하는 ODBC가 아닌 연결 문자열을 암호화합니다.
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
```

첫 번째 명령은 **ConvertTo-SecureString을** 사용하여 지정된 연결 문자열을 보안 문자열 개체로 변환한 다음 해당 개체를 $Value 저장합니다.
두 번째 명령은 Get-Credential cmdlet을 사용하여 windows 인증(사용자 이름 및 암호)을 수집한 다음 해당 **PSCredential** 개체를 $Credential 저장합니다.
자세한 내용은 `Get-Help Get-Credential` .를 입력합니다.
세 번째 명령은 지정된 데이터 팩터리, 게이트웨이$Credential 리소스 그룹 및 연결된 서비스 유형에 대해 $Value 및 $Credential 개체에 대해 암호화된 값을 만듭니다.

### 예제 3: 파일 시스템 연결된 서비스에 대한 서버 이름 및 자격 증명 암호화
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

첫 번째 명령은 **ConvertTo-SecureString을** 사용하여 지정된 문자열을 보안 문자열로 변환한 다음 해당 개체를 $Value 저장합니다.
두 번째 명령은 **Get-Credential을** 사용하여 Windows 인증(사용자 이름 및 암호)을 수집한 다음 해당 **PSCredential** 개체를 $Credential 저장합니다.
세 번째 명령은 지정된 데이터 팩터리, 게이트웨이$Credential 리소스 그룹 및 연결된 서비스 유형에 대해 $Value 및 $Credential 개체에 대해 암호화된 값을 만듭니다.

### 예제 4: HDFS 연결된 서비스에 대한 자격 증명 암호화
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

**ConvertTo-SecureString** 명령은 지정된 문자열을 보안 문자열로 변환합니다.
**New-Object** 명령은 보안 사용자 이름 및 암호 문자열을 사용하여 PSCredential 개체를 만듭니다.
대신 **Get-Credential** 명령을 사용하여 Windows 인증(사용자 이름 및 암호)을 수집한 다음 이전 예제와 같이 반환된 **PSCredential** 개체를 $credential 변수에 저장할 수 있습니다.
**New-AzDataFactoryEncryptValue** 명령은 지정된 데이터 팩터리, 게이트웨이$Credential 리소스 그룹 및 연결된 서비스 유형에 대해 $Credential 개체에 대해 암호화된 값을 만듭니다.

### 예제 5: ODBC 연결된 서비스에 대한 자격 증명 암호화
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

**ConvertTo-SecureString** 명령은 지정된 문자열을 보안 문자열로 변환합니다.
**New-AzDataFactoryEncryptValue** 명령은 지정된 데이터 팩터리, 게이트웨이$Value 리소스 그룹 및 연결된 서비스 유형에 대해 $Value 개체에 대해 암호화된 값을 만듭니다.

## PARAMETERS

### -AuthenticationType
데이터 원본에 연결하는 데 사용할 인증 유형을 지정합니다.
이 매개 변수에 허용되는 값은
- Windows
- 기본
- 익명.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Basic, Anonymous

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
사용할 Windows 인증 자격 증명(사용자 이름 및 암호)을 지정합니다.
이 cmdlet은 여기에서 지정한 자격 증명 데이터를 암호화합니다.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Database
연결된 서비스의 데이터베이스 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataFactory
**PSDataFactory 개체를 지정합니다.**
이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 대한 데이터를 암호화합니다.

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
데이터 팩터리의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 대한 데이터를 암호화합니다.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GatewayName
게이트웨이의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 게이트웨이에 대한 데이터를 암호화합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NonCredentialValue
ODBC(Open Database Connectivity) 연결 문자열의 비 자격 증명 부분을 지정합니다.
이 매개 변수는 ODBC 연결된 서비스에만 적용할 수 있습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Azure 리소스 그룹의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 그룹에 대한 데이터를 암호화합니다.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Server
연결된 서비스의 서버 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
연결된 서비스 유형을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 연결된 서비스 형식에 대한 데이터를 암호화합니다.
이 매개 변수에 허용되는 값은
- OnPremisesSqlLinkedService 
- OnPremisesFileSystemLinkedService 
- OnPremisesOracleLinkedService 
- OnPremisesOdbcLinkedService 
- OnPremisesPostgreSqlLinkedService 
- OnPremisesTeradataLinkedService 
- OnPremisesMySQLLinkedService 
- OnPremisesDB2LinkedService 
- OnPremisesSybaseLinkedService

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OnPremisesSqlLinkedService, OnPremisesFileSystemLinkedService, OnPremisesOracleLinkedService, OnPremisesOdbcLinkedService, OnPremisesPostgreSqlLinkedService, OnPremisesTeradataLinkedService, OnPremisesMySQLLinkedService, OnPremisesDB2LinkedService, OnPremisesSybaseLinkedService, HdfsLinkedService

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Value
암호화할 값을 지정합니다.
연결된 서비스 및 SQL Server Oracle 연결된 서비스의 경우 연결 문자열을 사용 합니다.
On-premises ODBC 연결된 서비스의 경우 연결 문자열의 자격 증명 부분을 사용 합니다.
프레미스 파일 시스템 연결된 서비스의 경우 파일 시스템이 게이트웨이 컴퓨터에 로컬인 경우 Local 또는 localhost를 사용하며 파일 시스템이 게이트웨이 컴퓨터와 다른 서버에 있는 경우 서버 \\ \\ 이름을 사용 합니다.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## 출력

### System.String

## 참고 사항
* 키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리

## 관련 링크

[New-AzDataFactoryEncryptValue](./New-AzDataFactoryEncryptValue.md)


