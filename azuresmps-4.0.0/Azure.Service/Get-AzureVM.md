---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BBA0D5D3-29A5-4E00-9075-702E2F81CA52
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcff7873042d9f7a07eee26f93312c8690e16416
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046547"
---
# Get-AzureVM

## SYNOPSIS
하나 이상의 Azure 가상 컴퓨터에서 정보를 검색 합니다.

## 구문과

### ListAllVMs (기본값)
```
Get-AzureVM [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### GetVMByServiceAndVMName
```
Get-AzureVM [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**Get-help** Cmdlet은 Azure에서 실행 되는 가상 컴퓨터에 대 한 정보를 검색 합니다.
특정 가상 컴퓨터에 대 한 정보를 포함 하는 개체를 반환 하거나, 현재 구독에 대해 지정 된 서비스의 모든 가상 컴퓨터에 대해 가상 컴퓨터를 지정 하지 않은 경우이 작업을 시작 합니다.

## 예제의

### 예제 1: 지정 된 가상 컴퓨터에서 정보 검색
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "VirtualMachine02"
```

이 명령은 ContosoService01 클라우드 서비스에서 실행 되는 VirtualMachine02 가상 컴퓨터에 대 한 정보가 포함 된 개체를 반환 합니다.

### 예제 2: 모든 가상 컴퓨터에 대 한 정보 검색
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"
```

이 명령은 ContosoService01 클라우드 서비스에서 실행 되는 모든 가상 컴퓨터에 대 한 정보를 사용 하 여 목록 개체를 검색 합니다.

### 예제 3: 가상 컴퓨터 상태 테이블 표시
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"  | Format-Table AutoSize -Property "Name",@{Expression={$_.InstanceUpgradeDomain};Label="UpgDom";Align="Right"},"InstanceStatus"
```

이 명령은 ContosoService01 서비스에서 실행 되는 가상 컴퓨터, 해당 업그레이드 도메인, 각 가상 컴퓨터의 현재 상태를 보여 주는 테이블을 표시 합니다.

## 변수

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

### -이름
정보를 검색할 가상 컴퓨터의 이름을 지정 합니다.
이 매개 변수를 제공 하지 않는 경우 cmdlet은 지정 된 서비스의 모든 가상 컴퓨터에 대 한 정보를 포함 하는 list 개체를 반환 합니다.

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -ServiceName
가상 컴퓨터 정보를 반환할 클라우드 서비스의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[뉴욕](./New-AzureVM.md)

[새로운 AzureVMConfig](./New-AzureVMConfig.md)

[제거-Add-azurevm](./Remove-AzureVM.md)

[-Add-azurevm 다시 시작](./Restart-AzureVM.md)

[시작-Add-azurevm](./Start-AzureVM.md)

[-Add-azurevm](./Stop-AzureVM.md)

[업데이트-Add-azurevm](./Update-AzureVM.md)


