---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
ms.openlocfilehash: c51740ef111c0efe2f05c71d55ab5d3f076ac9d2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041856"
---
# Get-AzADServicePrincipal

## SYNOPSIS
Active directory 서비스 사용자를 필터링 합니다.

## 구문과

### EmptyParameterSet (기본값)
```
Get-AzADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### SearchStringParameterSet
```
Get-AzADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### DisplayNameParameterSet
```
Get-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### ObjectIdParameterSet
```
Get-AzADServicePrincipal -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### ApplicationIdParameterSet
```
Get-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### ApplicationObjectParameterSet
```
Get-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### SPNParameterSet
```
Get-AzADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## 설명은
Active directory 서비스 사용자를 필터링 합니다.

## 예제의

### 예제 1-광고 서비스 사용자 목록 표시

```
PS C:\> Get-AzADServicePrincipal
```

테 넌 트에서 모든 광고 서비스 사용자를 나열 합니다.

### 예제 2-페이징을 사용 하 여 광고 서비스 사용자 나열

```
PS C:\> Get-AzADServicePrincipal -First 100
```

테 넌 트에서 첫 번째 100 광고 서비스 사용자를 나열 합니다.

### 예제 3-SPN을 기준으로 서비스 사용자 나열

```
PS C:\> Get-AzADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

SPN이 ' 36f81fc3-b00f-48cd-8218-3879f51ff39f ' 인 서비스 사용자를 나열 합니다.

### 예제 4-검색 문자열을 기준으로 서비스 사용자 나열

```
PS C:\> Get-AzADServicePrincipal -SearchString "Web"
```

표시 이름이 "Web"으로 시작 하는 모든 광고 서비스 사용자를 나열 합니다.

### 예제 5-파이핑을 기준으로 서비스 사용자 나열

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzADServicePrincipal
```

개체 id가 ' 39e64ec6-569b-4030-8e1c-c3c519a05d69 ' 인 광고 응용 프로그램을 가져오고이를 Get-AzADServicePrincipal cmdlet에 파이프 하 여 해당 응용 프로그램의 모든 서비스 사용자를 나열 합니다.

## 변수

### -ApplicationId
서비스 사용자 응용 프로그램 id입니다.

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationObject
서비스 사용자가 검색 되 고 있는 응용 프로그램 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

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
서비스 사용자 표시 이름입니다.

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DisplayNameBeginsWith
서비스 사용자 검색 문자열입니다.

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: SearchString

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
서비스 사용자의 개체 id입니다.

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
서비스의 SPN입니다.

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IncludeTotalCount
데이터 집합의 개체 수를 보고 합니다. 현재이 매개 변수는 아무런 작업도 수행 하지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -생략
첫 N 개 개체를 무시 하 고 나머지 개체를 가져옵니다.

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -첫 번째
반환할 최대 개체 수입니다.

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### System. 문자열

### 시스템 Guid

### ActiveDirectory PSADApplication 프로그램

## 출력

### ActiveDirectory PSADServicePrincipal

## 상속자

## 관련 링크

[새로운 AzADServicePrincipal](./New-AzADServicePrincipal.md)

[Set-AzADServicePrincipal](./Set-AzADServicePrincipal.md)

[제거-AzADServicePrincipal](./Remove-AzADServicePrincipal.md)

[Get-AzADApplication](./Get-AzADApplication.md)

[Get-AzADSpCredential](./Get-AzADSpCredential.md)

