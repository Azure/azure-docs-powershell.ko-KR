---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: e7c77dc4daf38634e7661f4579dd5bbcc81d0443
ms.sourcegitcommit: e680033f216d86cd91a1dfdb8328d32f4c99d21a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/02/2021
ms.locfileid: "99251831"
---
# New-AzADServicePrincipal

## SYNOPSIS
새 Azure Active Directory 서비스 주체를 만듭니다.

## 구문

### SimpleParameterSet(기본값)

```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithoutCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ApplicationWithPasswordPlainParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithPasswordCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithKeyPlainParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithKeyCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithoutCredentialParameterSet

```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### DisplayNameWithPasswordPlainParameterSet

```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithPasswordCredentialParameterSet

```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithKeyPlainParameterSet

```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithKeyCredentialParameterSet

```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithPasswordPlainParameterSet

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithPasswordCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithKeyPlainParameterSet

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithKeyCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명

새 Azure Active Directory 서비스 주체를 만듭니다. 기본 매개 변수 집합은 매개 변수가 제공되지 않은 경우 기본값을 사용합니다. 기본값에 대한 자세한 내용은 각 매개 변수에 대한 설명을 참조하세요. 이 cmdlet에는 역할 및 범위 매개 변수를 사용하여 서비스 주체에 역할을 **할당할** **수** 있습니다. 둘 다 생략하면 기여자 역할이 서비스 주체에 할당됩니다. 역할 및 범위  매개  변수의 기본값은 현재 **구독에 대한** 참가자입니다. 이 cmdlet은 애플리케이션을 만들고 ApplicationId가 제공되지 않은 경우 해당 속성을 설정합니다. 애플리케이션별 매개 변수를 업데이트하기 위해 [Update-AzADApplication](./update-azadapplication.md) cmdlet을 사용합니다.

> [!WARNING]
> **New-AzADServicePrincipal** 명령을 사용하여 서비스 주체를 만들 때 출력에는 보호해야 하는 자격 증명이 포함됩니다. 또는 관리 ID를 [](/azure/active-directory/managed-identities-azure-resources/overview) 사용하여 자격 증명을 사용할 필요가 없습니다.
>
> 기본적으로 **New-AzADServicePrincipal은** 구독 [](/azure/role-based-access-control/built-in-roles#contributor) 범위의 서비스 주체에 기여자 역할을 할당합니다. 손상된 서비스 주체의 위험을 줄이기 위해 보다 구체적인 역할을 할당하고 리소스 또는 리소스 그룹으로 범위를 좁힐 수 있습니다. 자세한 [내용은 역할 할당을 추가하는](/azure/role-based-access-control/role-assignments-steps) 단계를 참조하세요.

## 예제

### 예제 1: 간단한 AD 서비스 주체 만들기

다음 예제에서는 지정되지 않은 매개 변수에 대한 기본값을 사용하여 AD 서비스 주체를 만듭니다. 애플리케이션 ID가 제공되지 않은 경우 서비스 주체에 대한 애플리케이션이 만들어집니다. 역할 또는 범위에 대한 값이 제공되지 않습니다.  생성된 서비스 주체에는 현재 구독에 대한 참가자 역할이 할당됩니다. 

```powershell
New-AzADServicePrincipal
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### 예제 2: 지정된 역할 및 기본 범위를 통해 간단한 AD 서비스 주체 만들기

다음 예제에서는 지정되지 않은 매개 변수에 대한 기본값을 사용하여 AD 서비스 주체를 만듭니다. 애플리케이션 ID가 제공되지 않은 경우 서비스 주체에 대한 애플리케이션이 만들어집니다. 범위 매개 변수에  대한 값이 제공되지 않고 현재 구독에 대한 읽기 권한자 권한으로 서비스 **주체가** 만들어집니다.

```powershell
New-AzADServicePrincipal -Role Reader
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000' to the new service principal.
```

### 예제 3: 지정된 범위 및 기본 역할을 통해 간단한 AD 서비스 주체 만들기

다음 예제에서는 지정되지 않은 매개 변수에 대한 기본값을 사용하여 AD 서비스 주체를 만듭니다. 애플리케이션 ID가 제공되지 않은 경우 서비스 주체에 대한 애플리케이션이 만들어집니다. 서비스 주체는  역할 매개 변수에 대한 값이 제공되지 않고 제공된 리소스 그룹 범위에 대한 참가자 권한으로 **만들어집니다.**

```powershell
New-AzADServicePrincipal -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### 예제 4: 지정된 범위 및 역할을 통해 간단한 AD 서비스 주체 만들기

다음 예제에서는 지정되지 않은 매개 변수에 대한 기본값을 사용하여 AD 서비스 주체를 만듭니다. 애플리케이션 ID가 제공되지 않은 경우 서비스 주체에 대한 애플리케이션이 만들어집니다. 서비스 주체는 제공된 리소스 그룹 범위에 **대한 읽기** 권한자 권한으로 만들어집니다.

```powershell
New-AzADServicePrincipal -Role Reader -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### 예제 5: 역할 할당과 함께 애플리케이션 ID를 사용하여 새 AD 서비스 주체 만들기

다음 예제에서는 애플리케이션 ID가 '000000000-0000-0000-0000-0000-000000000000'인 애플리케이션에 대한 새 AD 서비스 주체를 만듭니다. 역할 또는 범위에 대한 값이 제공되지 않습니다.  생성된 서비스 주체에는 현재 구독에 대한 참가자 역할이 할당됩니다. 

```powershell
New-AzADServicePrincipal -ApplicationId 00000000-0000-0000-0000-000000000000
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://my-temp-app}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : my-temp-app
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### 예제 6: 파이핑을 사용하여 새 AD 서비스 주체 만들기

다음 예제에서는 [Get-AzADApplication](./get-azadapplication.md) cmdlet을 사용하여 개체 ID '3ede3c26-b443-4e0b-9efc-b05e68338dc3'을 사용하여 애플리케이션을 검색합니다. 결과는 cmdlet에 파이프하여 애플리케이션에 대한 새 AD 서비스 `New-AzADServicePrincipal` 주체를 생성합니다.

```powershell
Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

### 예제 7: DisplayName 및 암호 자격 증명을 사용하여 새 AD 서비스 주체 만들기

다음 예제에서는 **ServicePrincipalName** 이름과 **StrongPassworld!23의** 암호를 사용하여 새 애플리케이션을 만듭니다. 생성된 애플리케이션을 기반으로 서비스 주체가 만들어집니다. 시작 날짜 및 종료 날짜가 암호 자격 증명에 추가됩니다.

```powershell
$credentials = New-Object -TypeName Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{
  StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password='StrongPassworld!23'}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000c
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

### 예제 8: DisplayName 및 일반 키 자격 증명을 사용하여 새 AD 서비스 주체 만들기

다음 예제에서는 **ServicePrincipalName** 이름과 인증서 이름을 지정하여 새 애플리케이션을 **$cert.** 만든 애플리케이션을 기반으로 서비스 주체가 만들어집니다. 종료 날짜가 키 자격 증명에 추가됩니다.

```powershell
$cert = 'public certificate as Base64 encoded string'
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert  -EndDate '2021-01-01'
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

## PARAMETERS

### -ApplicationId

테넌트의 서비스 주체에 대한 고유한 애플리케이션 ID입니다. 만든 후 이 속성을 변경할 수 없습니다. 기존 애플리케이션에 대한 애플리케이션 ID를 지정하지 않으면 애플리케이션이 만들어집니다.

```yaml
Type: System.Guid
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationObject

서비스 주체가 생성되는 애플리케이션을 나타내는 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CertValue

비대칭 자격 증명 형식의 값입니다. Base64로 인코딩된 인증서를 나타났습니다.

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile

Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -DisplayName

서비스 주체의 이름입니다. 표시 이름을 지정하지 않은 경우 이 값은 기본적으로 접미사는 애플리케이션을 만들 때인 **azure-powershell-MM-dd-yy-HH-mm-ss로** 설정됩니다.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndDate

자격 증명 사용의 유효 종료 날짜입니다. 기본 종료 날짜 값은 오늘부터 1년입니다.
비대칭 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 또는 그 이전으로 설정해야 합니다.

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyCredential

애플리케이션과 연결된 키 자격 증명의 컬렉션입니다.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PasswordCredential

애플리케이션과 연결된 암호 자격 증명의 컬렉션입니다.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Role

서비스 주체가 범위를 통해 있는 역할입니다. 값이 제공되지 않고 **역할은** 기본적으로 기여자 **역할로 설정됩니다.**

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Scope

서비스 주체에 대한 권한이 있는 범위입니다. 값이 제공되지 않고 **범위는** 기본적으로 현재 구독으로 설정됩니다.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipAssignment

설정된 경우 서비스 주체에 대한 기본 역할 할당 만들기를 건너뜁.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartDate

자격 증명 사용의 유효 시작 날짜입니다. 기본 시작 날짜 값은 오늘입니다. 비대칭 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 또는 그 이후로 설정해야 합니다.

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

cmdlet이 실행되는 경우의 결과 표시 cmdlet이 실행되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](/powershell/module/microsoft.powershell.core/about/about_commonparameters)about_CommonParameters.
## 입력

### System.Guid

### System.String

### Microsoft.Azure.Commands.ActiveDirectory.PSADApplication

### Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]

### Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]

### System.DateTime

## 출력

### Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper

## 참고 사항

키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 리소스, 그룹, 템플릿, 배포

## 관련 링크

[Remove-AzADServicePrincipal](./Remove-AzADServicePrincipal.md)

[Get-AzADServicePrincipal](./Get-AzADServicePrincipal.md)

[New-AzADApplication](./New-AzADApplication.md)

[Remove-AzADApplication](./Remove-AzADApplication.md)

[Get-AzADSpCredential](./Get-AzADSpCredential.md)

[New-AzADSpCredential](./New-AzADSpCredential.md)

[Remove-AzADSpCredential](./Remove-AzADSpCredential.md)