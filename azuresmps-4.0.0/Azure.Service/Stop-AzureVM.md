---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4F347DD1-907C-47DB-8F1D-636DE031A56A
online version: ''
schema: 2.0.0
ms.openlocfilehash: e01265cf3db8a0dc3fd9d74a4a263a20965b10fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045741"
---
# Stop-AzureVM

## SYNOPSIS
Azure 가상 컴퓨터를 종료 합니다.

## 구문과

### ByName (기본값)
```
Stop-AzureVM [-Name] <String[]> [-StayProvisioned] [-Force] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### 의견
```
Stop-AzureVM -VM <IPersistentVM[]> [-StayProvisioned] [-Force] [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## 설명은
이 **(가) add-azurevm** cmdlet이 가상 컴퓨터를 종료 합니다.

## 예제의

### 예제 1: 가상 컴퓨터 종료
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM"
```

이 명령은 지정 된 서비스가 포함 하는 가상 컴퓨터를 종료 합니다.

### 예제 2: 가상 컴퓨터 개체를 사용 하 여 가상 컴퓨터 종료
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "MyVM" | Stop-AzureVM
```

이 명령은 지정 된 서비스가 포함 하는 가상 컴퓨터를 종료 하는 데 사용 되는 가상 컴퓨터 개체를 통해 **시작** 합니다.

### 예제 3: VM을 종료 하 고 VM을 프로 비전 된 상태로 유지
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -StayProvisioned
```

이 명령은 지정 된 서비스에 포함 되어 있는 가상 컴퓨터를 종료 하 고 계속 프로 비전 합니다.

### 예제 4: VM 종료 및 배포에서 마지막 VM의 할당 취소 허용
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -Force
```

이 명령은 지정 된 서비스가 포함 하는 가상 컴퓨터를 종료 하 고 배포의 마지막 가상 컴퓨터에 대 한 할당 취소를 허용 합니다.

### 예제 5: 여러 Vm 종료
```
PS C:\> Stop-AzureVM -ServiceName "PSTestService" -Name "*" -Force
```

이 명령은 지정 된 서비스에 포함 되어 있는 여러 가상 컴퓨터를 종료 합니다.

## 변수

### -Force
배포에서 마지막 가상 컴퓨터의 할당 취소를 허용할지 여부를 지정 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
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

### -이름
종료할 가상 컴퓨터의 이름을 지정 합니다.

와일드 카드 문자를 사용 하 여 여러 가상 컴퓨터를 비동기적으로 중지할 수 있습니다.
와일드 카드 문자를 사용 하는 경우이 cmdlet은 종료 역할 작업 https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx) https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx) .

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: 

Required: True
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
종료할 가상 컴퓨터를 포함 하는 Azure 서비스의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StayProvisioned
이 cmdlet이 가상 컴퓨터를 프로 비전 된 상태로 유지 하도록 지정 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
종료할 가상 컴퓨터를 식별 하는 가상 컴퓨터 개체를 지정 합니다.

```yaml
Type: IPersistentVM[]
Parameter Sets: Input
Aliases: InputObject

Required: True
Position: Named
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

[다운로드-Add-azurevm](./Get-AzureVM.md)

[뉴욕](./New-AzureVM.md)

[-Add-azurevm 다시 시작](./Restart-AzureVM.md)

[시작-Add-azurevm](./Start-AzureVM.md)


