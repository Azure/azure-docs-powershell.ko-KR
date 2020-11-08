---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3249E908-B1D9-4707-844D-168274F1A466
online version: ''
schema: 2.0.0
ms.openlocfilehash: ae16609adf70b2e5a0edcd05c36b30860a3920cf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045825"
---
# <span data-ttu-id="321f0-101">Set-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="321f0-101">Set-AzureReservedIPAssociation</span></span>

## <span data-ttu-id="321f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="321f0-102">SYNOPSIS</span></span>
<span data-ttu-id="321f0-103">예약 된 IP 주소를 기존 가상 머신 또는 클라우드 서비스와 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="321f0-103">Associates a reserved IP address with an existing virtual machine or cloud service.</span></span>

## <span data-ttu-id="321f0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="321f0-104">SYNTAX</span></span>

```
Set-AzureReservedIPAssociation [-ReservedIPName] <String> [-ServiceName] <String> [[-VirtualIPName] <String>]
 [[-Slot] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="321f0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="321f0-105">DESCRIPTION</span></span>
<span data-ttu-id="321f0-106">**AzureReservedIPAssociation** cmdlet은 예약 된 IP 주소를 실행 중인 가상 머신 또는 클라우드 서비스의 VIP (가상 ip) 주소와 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="321f0-106">The **Set-AzureReservedIPAssociation** cmdlet associates a reserved IP address with the Virtual IP address (VIP) of a running virtual machine or cloud service.</span></span>
<span data-ttu-id="321f0-107">예약 된 IP 주소는이 cmdlet을 호출할 때 사용 되지 않아야 하 고 가상 머신 또는 클라우드 서비스와 동일한 지역에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="321f0-107">The reserved IP address must not be in use at the time of invocation of this cmdlet, and must be in the same region as the virtual machine or cloud service.</span></span>

<span data-ttu-id="321f0-108">예약 된 IP 주소를 사용 하 여 가상 컴퓨터 또는 서비스에 액세스할 수 있는 작업은 완료 하는 데 약 30 초가 걸립니다.</span><span class="sxs-lookup"><span data-stu-id="321f0-108">The operation takes about 30 seconds to complete, after which the virtual machine or service is accessible using the reserved IP address.</span></span>

## <span data-ttu-id="321f0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="321f0-109">EXAMPLES</span></span>

### <span data-ttu-id="321f0-110">예제 1: 예약 된 IP 연결 설정</span><span class="sxs-lookup"><span data-stu-id="321f0-110">Example 1: Set a reserved IP association</span></span>
```
PS C:\> Set-AzureReservedIPAssociation -ReservedIPName "ResIp14" -ServiceName "PipTestWestEurope"
```

<span data-ttu-id="321f0-111">이 명령은 ResIp14 이라는 예약 된 IP 주소를 서비스 PipTestWestEurope에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="321f0-111">This command assigns the reserved IP address named ResIp14 to the service PipTestWestEurope.</span></span>
<span data-ttu-id="321f0-112">ResIp14는 서유럽 지역에 예약 된 IP입니다.</span><span class="sxs-lookup"><span data-stu-id="321f0-112">ResIp14 is a reserved IP in the West Europe region.</span></span>

## <span data-ttu-id="321f0-113">변수</span><span class="sxs-lookup"><span data-stu-id="321f0-113">PARAMETERS</span></span>

### <span data-ttu-id="321f0-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="321f0-114">-InformationAction</span></span>
<span data-ttu-id="321f0-115">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="321f0-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="321f0-116">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="321f0-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="321f0-117">하기로</span><span class="sxs-lookup"><span data-stu-id="321f0-117">Continue</span></span>
- <span data-ttu-id="321f0-118">숨기기</span><span class="sxs-lookup"><span data-stu-id="321f0-118">Ignore</span></span>
- <span data-ttu-id="321f0-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="321f0-119">Inquire</span></span>
- <span data-ttu-id="321f0-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="321f0-120">SilentlyContinue</span></span>
- <span data-ttu-id="321f0-121">중지가</span><span class="sxs-lookup"><span data-stu-id="321f0-121">Stop</span></span>
- <span data-ttu-id="321f0-122">대기</span><span class="sxs-lookup"><span data-stu-id="321f0-122">Suspend</span></span>

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

### <span data-ttu-id="321f0-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="321f0-123">-InformationVariable</span></span>
<span data-ttu-id="321f0-124">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="321f0-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="321f0-125">-프로필</span><span class="sxs-lookup"><span data-stu-id="321f0-125">-Profile</span></span>
<span data-ttu-id="321f0-126">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="321f0-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="321f0-127">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="321f0-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="321f0-128">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="321f0-128">-ReservedIPName</span></span>
<span data-ttu-id="321f0-129">가상 머신 또는 서비스와 연결할 예약 된 IP 주소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="321f0-129">Specifies the name of the reserved IP address to associate with a virtual machine or service.</span></span>

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

### <span data-ttu-id="321f0-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="321f0-130">-ServiceName</span></span>
<span data-ttu-id="321f0-131">예약 된 IP 주소를 연결 하는 데 사용할 배포를 보유 하 고 있는 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="321f0-131">Specifies the name of the service that has the deployment with which to associate the reserved IP address.</span></span>

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

### <span data-ttu-id="321f0-132">-슬롯</span><span class="sxs-lookup"><span data-stu-id="321f0-132">-Slot</span></span>
<span data-ttu-id="321f0-133">배포 슬롯을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="321f0-133">Specifies the deployment slot.</span></span>
<span data-ttu-id="321f0-134">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="321f0-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="321f0-135">대기</span><span class="sxs-lookup"><span data-stu-id="321f0-135">Staging</span></span>
- <span data-ttu-id="321f0-136">프로덕션용</span><span class="sxs-lookup"><span data-stu-id="321f0-136">Production</span></span>

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

### <span data-ttu-id="321f0-137">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="321f0-137">-VirtualIPName</span></span>
<span data-ttu-id="321f0-138">예약 된 IP와 연결할 기존 VIP의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="321f0-138">Specifies the name of an existing VIP to associate with a reserved IP.</span></span>
<span data-ttu-id="321f0-139">클라우드 서비스에 Vip를 추가 하려면 Add-AzureVirtualIP을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="321f0-139">See Add-AzureVirtualIP to add VIPs to your cloud service.</span></span>

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

### <span data-ttu-id="321f0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="321f0-140">CommonParameters</span></span>
<span data-ttu-id="321f0-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="321f0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="321f0-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="321f0-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="321f0-143">입력</span><span class="sxs-lookup"><span data-stu-id="321f0-143">INPUTS</span></span>

## <span data-ttu-id="321f0-144">출력</span><span class="sxs-lookup"><span data-stu-id="321f0-144">OUTPUTS</span></span>

### <span data-ttu-id="321f0-145">WindowsAzure. 유틸리티. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="321f0-145">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="321f0-146">상속자</span><span class="sxs-lookup"><span data-stu-id="321f0-146">NOTES</span></span>

## <span data-ttu-id="321f0-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="321f0-147">RELATED LINKS</span></span>

[<span data-ttu-id="321f0-148">제거-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="321f0-148">Remove-AzureReservedIPAssociation</span></span>](./Remove-AzureReservedIPAssociation.md)


