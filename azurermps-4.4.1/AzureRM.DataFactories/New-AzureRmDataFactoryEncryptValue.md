---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 5BF24BC2-DEB6-4830-BDEA-841BAB070388
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryEncryptValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryEncryptValue.md
ms.openlocfilehash: 54a759370f39dcd3844d42d858d23f6c178a4d08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702706"
---
# New-AzureRmDataFactoryEncryptValue

## SYNOPSIS
중요 한 데이터를 암호화 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ByFactoryName (기본값)
```
New-AzureRmDataFactoryEncryptValue [-DataFactoryName] <String> [[-Value] <SecureString>]
 [[-GatewayName] <String>] [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
New-AzureRmDataFactoryEncryptValue [-DataFactory] <PSDataFactory> [[-Value] <SecureString>]
 [[-GatewayName] <String>] [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmDataFactoryEncryptValue** cmdlet은 암호나 Microsoft SQL Server 연결 문자열과 같은 중요 한 데이터를 암호화 하 고 암호화 된 값을 반환 합니다.

## 예제의

### 예제 1: 비 ODBC 연결 문자열 암호화
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzureRmDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

첫 번째 명령은 ConvertTo-SecureString cmdlet을 사용 하 여 지정 된 연결 문자열을 **SecureString** 개체로 변환한 다음 해당 개체를 $Value 변수에 저장 합니다.
자세한 내용은을 입력 `Get-Help ConvertTo-SecureString` 하세요.
허용 되는 값: SQL Server 또는 Oracle 연결 문자열입니다.

두 번째 명령은 지정 된 data factory, gateway, 리소스 그룹 및 연결 된 서비스 유형에 대해 $Value에 저장 된 개체에 대 한 암호화 값을 만듭니다.

### 예제 2: Windows 인증을 사용 하는 비 ODBC 연결 문자열을 암호화 합니다.
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzureRmDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;Integrated Security=True' -AsPlainText -Force
```

첫 번째 명령은 **ConvertTo** 를 사용 하 여 지정 된 연결 문자열을 안전한 문자열 개체로 변환한 다음 해당 개체를 $Value 변수에 저장 합니다.

두 번째 명령은 Get-Credential cmdlet을 사용 하 여 windows 인증 (사용자 이름 및 암호)을 수집한 다음 해당 **PSCredential** 개체를 $Credential 변수에 저장 합니다.
자세한 내용은을 입력 `Get-Help Get-Credential` 하세요.

세 번째 명령은 $Value에 저장 되어 있고 지정 된 데이터 팩토리, 게이트웨이, 리소스 그룹 및 연결 된 서비스 유형에 대 한 $Credential에 대해 암호화 된 값을 만듭니다.

### 예제 3: 파일 시스템 연결 서비스에 대 한 서버 이름 및 자격 증명 암호화
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzureRmDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

첫 번째 명령은 **ConvertTo** 를 사용 하 여 지정 된 문자열을 보안 문자열로 변환한 다음 해당 개체를 $Value 변수에 저장 합니다.

두 번째 명령은 **자격 증명 가져오기 기능** 을 사용 하 여 windows 인증 (사용자 이름 및 암호)을 수집한 다음 해당 **PSCredential** 개체를 $Credential 변수에 저장 합니다.

세 번째 명령은 $Value에 저장 되어 있고 지정 된 데이터 팩토리, 게이트웨이, 리소스 그룹 및 연결 된 서비스 유형에 대 한 $Credential에 대해 암호화 된 값을 만듭니다.

### 예제 4: HDFS 연결 된 서비스에 대 한 자격 증명 암호화
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzureRmDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

**ConvertTo-SecureString** 명령은 지정 된 문자열을 보안 문자열로 변환 합니다.
**새 개체** 명령은 보안 사용자 이름 및 암호 문자열을 사용 하 여 PSCredential 개체를 만듭니다.
대신 **Get-Credential** 명령을 사용 하 여 windows 인증 (사용자 이름 및 암호)을 수집한 다음 이전 예제와 같이 $credential 변수에 반환 된 **PSCredential** 개체를 저장 합니다.

**AzureRmDataFactoryEncryptValue** 명령은 지정 된 데이터 팩토리, 게이트웨이, 리소스 그룹 및 연결 된 서비스 유형에 대해 $Credential에 저장 된 개체에 대 한 암호화 값을 만듭니다.

### 예제 5: ODBC 연결 된 서비스에 대 한 자격 증명 암호화
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzureRmDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

**ConvertTo-SecureString** 명령은 지정 된 문자열을 보안 문자열로 변환 합니다.

**AzureRmDataFactoryEncryptValue** 명령은 지정 된 데이터 팩토리, 게이트웨이, 리소스 그룹 및 연결 된 서비스 유형에 대해 $Value에 저장 된 개체에 대 한 암호화 값을 만듭니다.

## 변수

### -AuthenticationType
데이터 원본에 연결 하는 데 사용할 인증 유형을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 창을
- 기본적
- 공용.

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
사용할 Windows 인증 자격 증명 (사용자 이름 및 암호)을 지정 합니다.
이 cmdlet은 여기에서 지정 하는 자격 증명 데이터를 암호화 합니다.

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

### -데이터베이스
연결 된 서비스의 데이터베이스 이름을 지정 합니다.

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
**PSDataFactory** 개체를 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 대 한 데이터를 암호화 합니다.

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
Data factory의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 대 한 데이터를 암호화 합니다.

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

### --게이트웨이 이름
게이트웨이의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 게이트웨이에 대 한 데이터를 암호화 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credentialvalue
ODBC (Open Database Connectivity) 연결 문자열의 자격 증명이 아닌 부분을 지정 합니다.
이 매개 변수는 ODBC 연결 된 서비스에만 적용 됩니다.

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
Azure 리소스 그룹의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 그룹의 데이터를 암호화 합니다.

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

### -서버
연결 된 서비스의 서버 이름을 지정 합니다.

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
연결 된 서비스 유형을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 연결 된 서비스 유형의 데이터를 암호화 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

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

### -값
암호화할 값을 지정 합니다.
온-프레미스 SQL Server 연결 된 서비스 및 온-프레미스 Oracle 연결 된 서비스의 경우 연결 문자열을 사용 합니다.
온-프레미스 ODBC 연결 서비스의 경우 연결 문자열의 자격 증명 부분을 사용 합니다.
온-프레미스 파일 시스템 연결 서비스의 경우 파일 시스템이 게이트웨이 컴퓨터에 로컬인 경우 Local 또는 localhost를 사용 하 고, 파일 시스템이 게이트웨이 컴퓨터와 다른 서버에 있는 경우 servername을 사용 \\ \\ 합니다.

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

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### System. 문자열

## 상속자
* 키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리

## 관련 링크

[새로운 AzureRmDataFactoryEncryptValue](./New-AzureRmDataFactoryEncryptValue.md)


