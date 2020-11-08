---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
ms.openlocfilehash: 402d781c32b98362d504dd5167024932d82e64fb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214992"
---
# New-AzEventGridTopic

## SYNOPSIS
새 Azure 이벤트 그리드 항목을 만듭니다.

## 구문과

```
New-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-InputSchema <String>] [-InputMappingField <Hashtable>] [-InputMappingDefaultValue <Hashtable>]
 [-InboundIpRule <Hashtable>] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
새 Azure 이벤트 그리드 항목을 만듭니다. 항목이 만들어지면 응용 프로그램에서 항목 끝점에 이벤트를 게시할 수 있습니다.

## 예제의

### 예제 1
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

\` \` \` \` 리소스 그룹 MyResourceGroupName에서 지정 된 지리적 위치 Westus2에 Topic1 \` 이벤트 그리드 항목을 만듭니다 \` .

### 예제 2
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

지정 된 \` \` \` \` \` \` 태그 "부서" 및 "환경"이 있는 리소스 그룹 MyResourceGroupName의 지정 된 지리적 위치 westus2에 Topic1 이벤트 그리드 항목을 만듭니다.

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

### -InboundIpRule
인바운드 IP 규칙의 목록을 나타내는 해시 테이블입니다. 각 규칙은 IP 주소를 CIDR 표기법으로 지정 합니다 (예: 10.0.0.0/8). 일치 여부를 기준으로 수행 되는 해당 작업과 함께 IpMask와 일치 하는 항목이 없습니다. 사용할 수 있는 작업 값에 허용만 포함

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputMappingDefaultValue
공백으로 구분 된 key = value 형식의 값으로 입력 매핑 필드를 나타내는 Hashtable입니다. 허용 되는 키 이름은 subject, eventtype 및 dataversion입니다. InputSchemaHelp만 customeventschema 경우 사용 됩니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputMappingField
공백으로 구분 된 key = value 형식의 입력 매핑 필드를 나타내는 Hashtable 허용 되는 키 이름은 id, topic, eventtime, subject, eventtype, dataversion입니다. InputSchemaHelp만 customeventschema 경우 사용 됩니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputSchema
항목에 대 한 입력 이벤트의 스키마입니다. 허용 되는 값은 eventgridschema, customeventschema 또는 cloudeventv01Schema입니다. 기본값은 eventgridschema입니다. Customeventschema가 지정 된 경우 InputMappingField 또는/및 InputMappingDefaultValue 매개 변수도 지정 해야 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EventGridSchema, CustomEventSchema, CloudEventSchemaV1_0

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -위치
주제의 위치

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
주제의 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicNetworkAccess
공용 네트워크를 통해 트래픽이 허용 되는지 여부를 결정 합니다. 기본적으로 사용 하도록 설정 되어 있습니다. InboundIpRule 매개 변수를 구성 하 여 특정 Ip로 제한할 수 있습니다. 허용 되는 값은 비활성화 되 고 사용 하도록 설정 됩니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
주제를 만들어야 하는 리소스 그룹입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### 태그
리소스 태그를 나타내는 Hashtables.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### System. 문자열

### System.webserver. 컬렉션 테이블

## 출력

### Microsoft. Azure. c c.

## 상속자

## 관련 링크
