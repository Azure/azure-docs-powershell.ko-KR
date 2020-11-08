---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 02DB15F5-5CE0-4FF0-8863-AF1B2BA5E775
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41f72ace02132ba4184af08e995404b47f76d0b0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045828"
---
# Set-AzureOSDisk

## SYNOPSIS
Azure 가상 컴퓨터의 호스트 캐시 모드를 수정 합니다.

## 구문과

### 로이 Esize
```
Set-AzureOSDisk [-HostCaching] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### 길이
```
Set-AzureOSDisk [[-HostCaching] <String>] [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## 설명은
**AzureOSDisk** Cmdlet은 Azure 가상 컴퓨터의 운영 체제 디스크에 대 한 호스트 캐시 모드를 수정 합니다.
지원 되는 호스트 캐시 모드는 ReadOnly 및 ReadWrite입니다.
실행 중인 가상 컴퓨터에서이 cmdlet을 실행 하면 해당 가상 컴퓨터가 다시 시작 됩니다.

## 예제의

### 예제 1: 파이프라인을 사용 하 여 호스트 캐시 모드를 ReadOnly로 설정
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02" | Set-AzureOSDisk -HostCaching "ReadOnly"
```

이 명령은 VirtualMachine02 cmdlet을 사용 하 여 ContosoService 이라는 서비스의 가상 컴퓨터 (이름 = **)** 를 가져옵니다.
이 명령은 파이프라인 연산자를 사용 하 여 가상 컴퓨터를 현재 cmdlet에 전달 합니다.
현재 cmdlet은 해당 가상 컴퓨터의 운영 체제 디스크에 대 한 호스트 캐시 모드를 읽기 전용으로 설정 합니다.

### 예제 2: 호스트 캐시 모드를 ReadWrite로 설정
```
PS C:\> $VM = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02"
PS C:\> Set-AzureOSDisk "ReadWrite" -VM $myVM2
```

첫 번째 명령은 ContosoService 이라는 서비스에서 VirtualMachine02 이라는 가상 컴퓨터를 가져온 다음 변수에 저장 합니다.

두 번째 명령은 해당 가상 컴퓨터의 운영 체제 디스크 호스트 캐시 모드를 ReadWrite로 설정 합니다.

## 변수

### -HostCaching
운영 체제 디스크에 대 한 호스트 캐시 특성을 지정 합니다.
유효한 값은 다음과 같습니다. 

- 읽기 
- 쓰기

```yaml
Type: String
Parameter Sets: NoResize
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Resize
Aliases: 

Required: False
Position: 0
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

### -ResizedSizeInGB
운영 체제 디스크의 새 크기 (기가바이트)를 지정 합니다.
크기는 현재 크기 보다 커야 합니다.

```yaml
Type: Int32
Parameter Sets: Resize
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
이 cmdlet이 운영 체제 디스크를 수정 하는 가상 컴퓨터를 지정 합니다.
가상 컴퓨터 개체를 가져오려면 **get-help** cmdlet을 사용 합니다.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[추가-AzureVMImage](./Add-AzureVMImage.md)

[Get-AzureOSDisk](./Get-AzureOSDisk.md)

[다운로드-Add-azurevm](./Get-AzureVM.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[Set AzureDataDisk](./Set-AzureDataDisk.md)

[업데이트-Add-azurevm](./Update-AzureVM.md)


