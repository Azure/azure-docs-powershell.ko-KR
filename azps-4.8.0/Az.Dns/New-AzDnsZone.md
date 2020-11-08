---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: dc110c8989951c6cf5a68e35fbc22c6545c84a1a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214996"
---
# New-AzDnsZone

## SYNOPSIS
새 DNS 영역을 만듭니다.

## 구문과

### Id (기본값)
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneId <String>]
 [-Tag <Hashtable>] [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 이름은
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneName <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 나타내는
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZone <DnsZone>]
 [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzDnsZone** cmdlet은 지정 된 리소스 그룹에 새 DNS (Domain Name System) 영역을 만듭니다. *Name* 매개 변수에 대해 고유한 DNS 영역 이름을 지정 해야 하며, cmdlet이 오류를 반환 합니다. 영역이 만들어지면 New-AzDnsRecordSet cmdlet을 사용 하 여 영역에서 레코드 집합을 만듭니다.
*확인* 매개 변수를 사용 하 여 Windows PowerShell 변수를 $ConfirmPreference 하 여 cmdlet에서 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.

## 예제의

### 예제 1: DNS 영역 만들기
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

이 명령은 지정 된 리소스 그룹에 myzone.com 이라는 새 DNS 영역을 만든 다음이를 $Zone 변수에 저장 합니다.

### 예제 2: 가상 네트워크 Id를 지정 하 여 개인 DNS 영역 만들기
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

이 명령은 지정 된 리소스 그룹에서 myprivatezone.com 이라는 새 개인 DNS 영역을 만들고 해당 ID를 지정 하 여 관련 된 해결 가상 네트워크를 만든 다음이를 $Zone 변수에 저장 합니다.

### 예제 3: 가상 네트워크 개체를 지정 하 여 개인 DNS 영역 만들기
```
PS C:\>$ResVirtualNetwork = Get-AzVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

이 명령은 연결 된 해결 가상 네트워크 ($ResVirtualNetwork 변수)를 사용 하 여 지정 된 리소스 그룹에 myprivatezone.com 이라는 새 개인 DNS 영역을 만든 다음 $Zone 변수에 저장 합니다.

### 예제 4: 부모 영역 이름을 지정 하 여 위임으로 DNS 영역 만들기
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneName "zone.com"
```

이 명령은 지정 된 리소스 그룹에 mychild.zone.com 이라는 새 자식 DNS 영역을 만들고 $Zone 변수에 저장 합니다.
또한 하위 영역과 동일한 구독 및 리소스 그룹에 상주 하는 zone.com 이라는 부모 DNS 영역에 위임을 추가 합니다.

### 예제 5: 부모 영역 id를 지정 하 여 위임으로 DNS 영역 만들기
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneId "/subscriptions/**67e2/resourceGroups/other-rg/providers/Microsoft.Network/dnszones/zone.com"
```

이 명령은 지정 된 리소스 그룹에 mychild.zone.com 이라는 새 자식 DNS 영역을 만들고 $Zone 변수에 저장 합니다.
또한 리소스 그룹의 zone.com 이라는 상위 DNS 영역에서 위임을 추가 합니다. 다른-rg 제공 된 구독은 생성 된 자식 영역의 경우와 동일 합니다.

### 예제 6: 부모 영역 개체를 지정 하 여 위임을 사용 하 여 DNS 영역 만들기
```
PS C:\>$PZone = New-AzDnsZone -Name "zone.com" -ResourceGroupName "MyResourceGroup" 
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZone @($PZone)
```

이 명령은 지정 된 리소스 그룹에 mychild.zone.com 이라는 새 자식 DNS 영역을 만들고 $Zone 변수에 저장 합니다.
또한 ParentZone 개체에 전달 된 zone.com 이라는 부모 DNS 영역에서 위임을 추가 합니다.

## 변수

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

### -이름
만들려는 DNS 영역의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ParentZone
위임을 추가할 부모 영역의 전체 이름입니다 (종료 점이 없음).

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ParentZoneId
위임을 추가할 상위 영역의 리소스 id (종료 점 없이)입니다.

```yaml
Type: System.String
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ParentZoneName
위임을 추가할 부모 영역의 전체 이름입니다 (종료 점이 없음).

```yaml
Type: System.String
Parameter Sets: Names
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RegistrationVirtualNetwork
이 DNS 영역에 가상 컴퓨터 호스트 이름 레코드를 등록할 가상 네트워크 목록으로, 개인 영역에만 사용할 수 있습니다.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RegistrationVirtualNetworkId
이 DNS 영역에 가상 컴퓨터 호스트 이름 레코드를 등록할 가상 네트워크 Id 목록으로, 개인 영역에만 사용할 수 있습니다.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResolutionVirtualNetwork
이 DNS 영역의 레코드를 확인할 수 있는 가상 네트워크 목록으로, 개인 영역에만 사용할 수 있습니다.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResolutionVirtualNetworkId
이 DNS 영역의 레코드를 확인할 수 있는 가상 네트워크 Id의 목록이 며, 개인 영역에만 사용할 수 있습니다.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
영역을 만들 리소스 그룹을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### 태그
해시 테이블 형태의 키-값 쌍입니다. 예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ZoneType
영역의 형식 (공개 또는 비공개)입니다. 형식이 나 공개 형식이 없는 영역은 DNS 계층에서 사용할 공용 DNS 처리 평면에서 사용할 수 있게 됩니다. 비공개 유형의 영역은 연결 된 가상 네트워크 집합 (이 기능은 미리 보기) 에서만 볼 수 있습니다. 이 속성은 영역에 대해 변경할 수 없습니다.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.ZoneType]
Parameter Sets: (All)
Aliases:
Accepted values: Public, Private

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### 시스템 Null 허용 ' 1 [[ZoneType, Microsoft azure. 관리. Dns, 버전 = 3.0.0.0, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]]

### System.webserver. 컬렉션 테이블

### System.webserver. List ' 1 [[System.webserver], CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]

### System.webserver. List ' 1 [[IResourceReference, Microsoft azure. 31bf3856ad364e35. 클라이언트. 네트워크, 버전 = 1.0.0.0, Culture = 중립, PublicKeyToken =]])

## 출력

### DnsZone에 대 한 명령

## 상속자
*확인* 매개 변수를 사용 하 여이 cmdlet이 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.
기본적으로 cmdlet은 $ConfirmPreference Windows PowerShell 변수의 값이 중간 인지 아래 인지 여부를 확인 하 라는 메시지를 표시 합니다.
*확인* 또는 *확인: $True* 를 지정 하는 경우이 cmdlet을 실행 하기 전에 확인 메시지가 표시 됩니다.
*확인: $False* 를 지정 하면 cmdlet에서 확인을 요구 하지 않습니다.

## 관련 링크

[Get-AzDnsZone](./Get-AzDnsZone.md)

[새로운 AzDnsRecordSet](./New-AzDnsRecordSet.md)

[제거-AzDnsZone](./Remove-AzDnsZone.md)
