---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADGroupMember.md
ms.openlocfilehash: f083498860f3f2b9e19280b41d953032796e0eb9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876502"
---
# Get-AzADGroupMember

## SYNOPSIS
현재 테 넌 트의 광고 그룹 구성원을 나열 합니다.

## 구문과

### ObjectIdParameterSet (기본값)
```
Get-AzADGroupMember [-GroupObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### DisplayNameParameterSet
```
Get-AzADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### GroupObjectParameterSet
```
Get-AzADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## 설명은
현재 테 넌 트의 광고 그룹 구성원을 나열 합니다.

## 예제의

### 예제 1-광고 그룹별 구성원 목록 개체 id

```
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

개체 id가 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' 인 AD 그룹의 구성원을 나열 합니다.

### 예제 2-페이징을 사용 하 여 광고 그룹 개체 id를 기준으로 구성원 나열

```
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

개체 id가 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' 인 AD 그룹의 첫 번째 100 구성원을 나열 합니다.

### 예제 3-파이핑을 기준으로 멤버 목록 표시

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzADGroupMember
```

개체 id가 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' 인 광고 그룹을 가져오고이를 Get-AzADGroupMember cmdlet에 파이프 하 여 해당 그룹의 모든 구성원을 나열 합니다. 

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

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

### -GroupDisplayName
그룹의 표시 이름입니다.

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GroupObject
구성원을 나열 하는 그룹 개체입니다.

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup
Parameter Sets: GroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -GroupObjectId
그룹의 개체 Id입니다.

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: Id, ObjectId

Required: False
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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 시스템 Guid

### Microsoft.Azure.Graph.RBAC.Version1_6 PSADGroup ActiveDirectory.
매개 변수: GroupObject (ByValue)

## 출력

### Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Ad개체

## 상속자

## 관련 링크

[Get-AzADUser](./Get-AzADUser.md)

[Get-AzADServicePrincipal](./Get-AzADServicePrincipal.md)

