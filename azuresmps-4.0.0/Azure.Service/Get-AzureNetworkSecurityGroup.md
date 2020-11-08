---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4E19A767-8233-42A0-95C5-1547B4DF297E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67c08105f8083b6b2e132c3b8e61c92627572305
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046334"
---
# Get-AzureNetworkSecurityGroup

## SYNOPSIS
네트워크 보안 그룹에 대 한 세부 정보를 가져옵니다.

## 구문과

```
Get-AzureNetworkSecurityGroup [-Name <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureNetworkSecurityGroup** Cmdlet은 Azure 네트워크 보안 그룹에 대 한 세부 정보를 반환 합니다.
*자세한* 매개 변수를 지정 하 여 네트워크 보안 규칙을 표시 합니다.

## 예제의

## 변수

### -세부 정보
이 cmdlet이 네트워크 보안 그룹에 대 한 네트워크 보안 규칙을 반환 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
이 cmdlet이 가져오는 네트워크 보안 그룹의 이름을 지정 합니다.

> [!NOTE]
> Azure 포털을 사용 하 여 ***기본 네트워킹*** 이외의 리소스 그룹에 클래식 네트워크 보안 그룹이 만들어지면 다음 PowerShell 구문을 사용 해야 합니다 `Get-AzureNetworkSecurityGroup -Name 'Group myResouceGroup myNetworkSecurityGroup'` .

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다.
프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases:

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

## 상속자

## 관련 링크

[새로운 AzureNetworkSecurityGroup](./New-AzureNetworkSecurityGroup.md)

[제거-AzureNetworkSecurityGroup](./Remove-AzureNetworkSecurityGroup.md)

