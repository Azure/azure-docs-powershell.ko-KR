---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A9E43722-DEE2-4A5C-A3F6-8DA6612735AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 34e6e98c2bf506e8102287251e18dceda4dd0c7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046432"
---
# Set-AzureAclConfig

## SYNOPSIS
ACL 구성 개체를 수정 합니다.

## 구문과

### AddRule
```
Set-AzureAclConfig [-AddRule] [-Action] <String> [-RemoteSubnet] <String> [[-Order] <Int32>]
 [[-Description] <String>] -ACL <NetworkAclObject> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### RemoveRule
```
Set-AzureAclConfig [-RemoveRule] [-RuleId] <Int32> -ACL <NetworkAclObject>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### SetRule
```
Set-AzureAclConfig [-SetRule] [-RuleId] <Int32> [[-Action] <String>] [[-RemoteSubnet] <String>]
 [[-Order] <Int32>] [[-Description] <String>] -ACL <NetworkAclObject> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**Set AzureAclConfig** cmdlet은 기존 Azure 가상 컴퓨터 구성에서 ACL (액세스 제어 목록) 구성 개체를 수정 합니다.

## 예제의

### 예제 1: 새 ACL 구성에 규칙 추가
```
PS C:\> $Acl = New-AzureAclConfig
PS C:\> Set-AzureAclConfig -AddRule -ACL $Acl -Action Permit -RemoteSubnet "172.0.0.0/8" -Order 100 -Description "Permit ACL rule"
```

첫 번째 명령은 ACL 구성을 만든 다음 $Acl 변수에 저장 합니다.

두 번째 명령은 $Acl에 저장 된 구성에 새 규칙을 추가 합니다.
명령에 규칙에 대 한 동작, 서브넷, 순서, 설명을 지정 합니다.

### 예제 2: ACL 구성에서 규칙 수정
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
PS C:\> Set-AzureAclConfig -SetRule -RuleId 0 -ACL $Acl -Order 102 -Description "Web endpoint rule"
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Set-AzureEndpoint -ACL $Acl -Name "Web" | Update-AzureVM
```

첫 번째 명령은 **VirtualMachine07 cmdlet을 사용 하 여 ContosoService** 이라는 이름의 서비스에서 가상 컴퓨터 이름을 가져옵니다.
이 명령은 파이프라인 연산자를 사용 하 여 해당 개체를 **Get AzureAclConfig** cmdlet에 전달 합니다.
해당 cmdlet은 Web 이라는 끝점에 대 한 ACL 구성을 가져옵니다.
명령은 $Acl 변수에 해당 ACL 구성 개체를 저장 합니다.

두 번째 명령은 ID가 0 인 규칙을 수정 합니다.
명령에서 규칙의 순서와 설명을 변경 합니다.

마지막 명령은 **Set AzureEndpoint** cmdlet을 사용 하 여 해당 가상 컴퓨터에 대 한 ACL 구성 개체를 설정 합니다.
또한이 명령은 해당 가상 컴퓨터를 업데이트 합니다.

### 예제 3: ACL 구성에서 규칙 제거
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
PS C:\> Set-AzureAclConfig -RemoveRule -ID 0 -ACL $Acl
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Set-AzureEndpoint -ACL $Acl -Name "Web" | Update-AzureVM
```

첫 번째 명령은 $Acl 변수에 ACL 구성 개체를 저장 합니다.
이는 이전 예제와 동일 합니다.

두 번째 명령은 $Acl의 ACL 구성에서 ID가 0 인 규칙을 제거 합니다.

마지막 명령은 가상 컴퓨터에 대 한 ACL 구성 개체를 설정 하 고 해당 가상 컴퓨터를 업데이트 합니다.
이는 이전 예제와 동일 합니다.

## 변수

### -ACL
이 cmdlet이 수정 하는 ACL 구성 개체를 지정 합니다.

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -작업
이 cmdlet이 추가 하거나 수정 하는 규칙에 대 한 작업을 지정 합니다.
유효한 값은 허용 및 거부입니다.

```yaml
Type: String
Parameter Sets: AddRule
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetRule
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddRule
이 cmdlet이 ACL 구성에 규칙을 추가 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: AddRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -설명
이 cmdlet이 추가 하거나 수정 하는 규칙에 대 한 설명을 지정 합니다.

```yaml
Type: String
Parameter Sets: AddRule, SetRule
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationAction
이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.

이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 하기로
- 숨기기
- Inquire
- SilentlyContinue
- 중지가
- 대기

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
정보 변수를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -주문
이 cmdlet이 추가 하거나 수정 하는 규칙의 처리 순서를 지정 합니다.

```yaml
Type: Int32
Parameter Sets: AddRule, SetRule
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoteSubnet
이 cmdlet이 추가 하거나 수정 하는 규칙에 대 한 원격 서브넷을 지정 합니다.
CIDR (클래스 없는 도메인간 라우팅) 형식의 주소를 지정 합니다.

```yaml
Type: String
Parameter Sets: AddRule
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetRule
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveRule
이 cmdlet이 ACL 구성에서 규칙을 제거 했음을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: RemoveRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RuleId
이 cmdlet이 ACL 구성에 대해 제거 하거나 수정 하는 규칙의 ID를 지정 합니다.

```yaml
Type: Int32
Parameter Sets: RemoveRule, SetRule
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SetRule
이 cmdlet이 ACL 구성의 규칙을 수정 하는 것을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: SetRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[Get-AzureAclConfig](./Get-AzureAclConfig.md)

[다운로드-Add-azurevm](./Get-AzureVM.md)

[새 AzureAclConfig](./New-AzureAclConfig.md)

[-AzureAclConfig 제거](./Remove-AzureAclConfig.md)

[Set-AzureEndpoint](./Set-AzureEndpoint.md)

[업데이트-Add-azurevm](./Update-AzureVM.md)


