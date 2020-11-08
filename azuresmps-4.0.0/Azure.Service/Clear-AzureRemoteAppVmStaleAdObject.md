---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DA8EC1BD-1219-4B98-B661-40A28897271F
online version: ''
schema: 2.0.0
ms.openlocfilehash: dcbca5ab73d64bd0336f723d623c7f976237ecba
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045703"
---
# Clear-AzureRemoteAppVmStaleAdObject

## SYNOPSIS
Azure Active Directory에서 더 이상 존재 하지 않는 Azure RemoteApp 가상 컴퓨터와 연결 된 개체를 제거 합니다.

## 구문과

```
Clear-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureRemoteAppVmStaleAdObject** cmdlet은 더 이상 존재 하지 않는 azure RemoteApp 가상 컴퓨터와 연결 된 Azure Active Directory의 개체를 제거 합니다.
Azure Active Directory 개체를 제거할 권한이 있는 자격 증명을 사용 해야 합니다.
*Verbose* 공용 매개 변수를 지정 하면이 cmdlet은 삭제 하는 각 개체의 이름을 표시 합니다.

## 예제의

### 예제 1: 컬렉션에 대 한 부실 개체 지우기
```
PS C:\> $AdminCredentials = Get-Credential
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso" -Credential $AdminCredentials
```

첫 번째 명령은 **Get-Credential** 을 사용 하 여 사용자 이름과 암호를 묻는 메시지를 표시 합니다.
명령이 $AdminCredentials 변수에 결과를 저장 합니다.

두 번째 명령은 Contoso 라는 컬렉션에 대 한 부실 개체를 지웁니다.
이 명령은 $AdminCredentials 변수에 저장 된 자격 증명을 사용 합니다.
명령이 제대로 수행 되려면 해당 자격 증명에 적절 한 권한이 있어야 합니다.

## 변수

### -CollectionName
Azure RemoteApp 컬렉션의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Credential
이 작업을 수행할 수 있는 권한이 있는 자격 증명을 지정 합니다.
**PSCredential** 개체를 가져오려면 **Get-Credential** cmdlet을 사용 합니다.
이 매개 변수를 지정 하지 않으면이 cmdlet은 현재 사용자 자격 증명을 사용 합니다.

```yaml
Type: PSCredential
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

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[Get-AzureRemoteAppVmStaleAdObject](./Get-AzureRemoteAppVmStaleAdObject.md)


