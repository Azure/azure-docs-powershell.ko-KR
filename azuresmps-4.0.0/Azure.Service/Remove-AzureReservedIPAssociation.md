---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A6964C80-1991-46FC-84C8-5B00616386BE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9e43f841fea77626c18edbda541fa011e95faceb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046136"
---
# <span data-ttu-id="3ac4f-101">Remove-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="3ac4f-101">Remove-AzureReservedIPAssociation</span></span>

## <span data-ttu-id="3ac4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ac4f-102">SYNOPSIS</span></span>
<span data-ttu-id="3ac4f-103">예약 된 IP 주소에서 VM 또는 클라우드 서비스로의 연결을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-103">Removes the association from the reserved IP address to the VM or cloud service.</span></span>

## <span data-ttu-id="3ac4f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3ac4f-104">SYNTAX</span></span>

```
Remove-AzureReservedIPAssociation [-ReservedIPName] <String> [-ServiceName] <String>
 [[-VirtualIPName] <String>] [[-Slot] <String>] [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3ac4f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3ac4f-105">DESCRIPTION</span></span>
<span data-ttu-id="3ac4f-106">AzureReservedIPAssociation cmdlet은 VM (가상 머신) 또는 클라우드 서비스에서 예약 된 IP 주소를 **분리** 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-106">The **Remove-AzureReservedIPAssociation** cmdlet disassociates a reserved IP address from a virtual machine (VM) or Cloud Service.</span></span>
<span data-ttu-id="3ac4f-107">작업이 완료 되 면 예약 된 IP 주소는 무료이 고 VM/VIP는 Azure 인벤토리에서 동적 공용 IP 주소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-107">When the operation completes, the reserved IP address is free and the VM/VIP gets a dynamic public IP Address from the Azure Inventory.</span></span>

## <span data-ttu-id="3ac4f-108">예제의</span><span class="sxs-lookup"><span data-stu-id="3ac4f-108">EXAMPLES</span></span>

### <span data-ttu-id="3ac4f-109">예제 1: 예약 된 IP 연결 제거</span><span class="sxs-lookup"><span data-stu-id="3ac4f-109">Example 1: Remove a reserved IP association</span></span>
```
PS C:\> Remove-AzureReservedIPAssociation -ReservedIPName "ResIp14" -ServiceName "PipTestWestEurope"
```

<span data-ttu-id="3ac4f-110">이 명령은 PipTestWestEurope 이라는 서비스에서 ResIp14 이라는 예약 된 IP 주소를 분리 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-110">This command disassociates the reserved IP address named ResIp14 from the service named PipTestWestEurope.</span></span>
<span data-ttu-id="3ac4f-111">PipTestWestEurope에 새 동적 VIP가 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-111">PipTestWestEurope will be assigned a new dynamic VIP.</span></span>

## <span data-ttu-id="3ac4f-112">변수</span><span class="sxs-lookup"><span data-stu-id="3ac4f-112">PARAMETERS</span></span>

### <span data-ttu-id="3ac4f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3ac4f-113">-Force</span></span>
<span data-ttu-id="3ac4f-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-114">Forces the command to run without asking for user confirmation.</span></span>

<span data-ttu-id="3ac4f-115">이 플래그를 사용 하 여 예약 된 IP 연결을 제거할 때 경고 메시지를 무시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-115">Use this flag to bypass warning messages when removing the reserved IP association.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ac4f-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3ac4f-116">-InformationAction</span></span>
<span data-ttu-id="3ac4f-117">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3ac4f-118">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3ac4f-119">하기로</span><span class="sxs-lookup"><span data-stu-id="3ac4f-119">Continue</span></span>
- <span data-ttu-id="3ac4f-120">숨기기</span><span class="sxs-lookup"><span data-stu-id="3ac4f-120">Ignore</span></span>
- <span data-ttu-id="3ac4f-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="3ac4f-121">Inquire</span></span>
- <span data-ttu-id="3ac4f-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3ac4f-122">SilentlyContinue</span></span>
- <span data-ttu-id="3ac4f-123">중지가</span><span class="sxs-lookup"><span data-stu-id="3ac4f-123">Stop</span></span>
- <span data-ttu-id="3ac4f-124">대기</span><span class="sxs-lookup"><span data-stu-id="3ac4f-124">Suspend</span></span>

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

### <span data-ttu-id="3ac4f-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3ac4f-125">-InformationVariable</span></span>
<span data-ttu-id="3ac4f-126">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3ac4f-127">-프로필</span><span class="sxs-lookup"><span data-stu-id="3ac4f-127">-Profile</span></span>
<span data-ttu-id="3ac4f-128">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3ac4f-129">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3ac4f-130">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="3ac4f-130">-ReservedIPName</span></span>
<span data-ttu-id="3ac4f-131">예약 된 IP 주소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-131">Specifies the name of the reserved IP address.</span></span>

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

### <span data-ttu-id="3ac4f-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3ac4f-132">-ServiceName</span></span>
<span data-ttu-id="3ac4f-133">서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-133">Specifies the  name of the service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ac4f-134">-슬롯</span><span class="sxs-lookup"><span data-stu-id="3ac4f-134">-Slot</span></span>
<span data-ttu-id="3ac4f-135">배포 환경을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-135">Specifies the deployment environment.</span></span>
<span data-ttu-id="3ac4f-136">이 매개 변수에 허용 되는 값은 프로덕션, 스테이징입니다.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-136">The acceptable values for this parameter are: Production, Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ac4f-137">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="3ac4f-137">-VirtualIPName</span></span>
<span data-ttu-id="3ac4f-138">서비스 또는 VM과의 연결을 제거할 가상 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-138">Specifies a virtual IP address from which to remove the association with a service or VM.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ac4f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ac4f-139">CommonParameters</span></span>
<span data-ttu-id="3ac4f-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ac4f-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ac4f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ac4f-142">입력</span><span class="sxs-lookup"><span data-stu-id="3ac4f-142">INPUTS</span></span>

## <span data-ttu-id="3ac4f-143">출력</span><span class="sxs-lookup"><span data-stu-id="3ac4f-143">OUTPUTS</span></span>

### <span data-ttu-id="3ac4f-144">WindowsAzure. 유틸리티. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="3ac4f-144">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="3ac4f-145">상속자</span><span class="sxs-lookup"><span data-stu-id="3ac4f-145">NOTES</span></span>

## <span data-ttu-id="3ac4f-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3ac4f-146">RELATED LINKS</span></span>

[<span data-ttu-id="3ac4f-147">Set-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="3ac4f-147">Set-AzureReservedIPAssociation</span></span>](./Set-AzureReservedIPAssociation.md)


