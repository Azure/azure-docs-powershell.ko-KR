---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9C22F5D7-1FD0-4699-83D7-1D72C5234DEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: d09173c43de9c01056055f714217db5eb4c58225
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045993"
---
# <span data-ttu-id="bfbe0-101">New-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="bfbe0-101">New-AzureReservedIP</span></span>

## <span data-ttu-id="bfbe0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfbe0-102">SYNOPSIS</span></span>
<span data-ttu-id="bfbe0-103">예약 된 IP 주소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-103">Creates a reserved IP address.</span></span>

## <span data-ttu-id="bfbe0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bfbe0-104">SYNTAX</span></span>

### <span data-ttu-id="bfbe0-105">CreateNewReservedIP (기본값)</span><span class="sxs-lookup"><span data-stu-id="bfbe0-105">CreateNewReservedIP (Default)</span></span>
```
New-AzureReservedIP [-ReservedIPName] <String> [[-Label] <String>] [-Location] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="bfbe0-106">CreateInUseReservedIPUsingSlot</span><span class="sxs-lookup"><span data-stu-id="bfbe0-106">CreateInUseReservedIPUsingSlot</span></span>
```
New-AzureReservedIP [-ReservedIPName] <String> [[-Label] <String>] [-Location] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="bfbe0-107">CreateInUseReservedIP</span><span class="sxs-lookup"><span data-stu-id="bfbe0-107">CreateInUseReservedIP</span></span>
```
New-AzureReservedIP [-ReservedIPName] <String> [[-Label] <String>] [-Location] <String> [-ServiceName] <String>
 [[-VirtualIPName] <String>] [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="bfbe0-108">설명은</span><span class="sxs-lookup"><span data-stu-id="bfbe0-108">DESCRIPTION</span></span>
<span data-ttu-id="bfbe0-109">**AzureReservedIP** cmdlet은 예약 된 IP 주소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-109">The **New-AzureReservedIP** cmdlet creates a reserved IP address.</span></span>

## <span data-ttu-id="bfbe0-110">예제의</span><span class="sxs-lookup"><span data-stu-id="bfbe0-110">EXAMPLES</span></span>

### <span data-ttu-id="bfbe0-111">예제 1: 새 예약 된 IP 만들기</span><span class="sxs-lookup"><span data-stu-id="bfbe0-111">Example 1: Create a new reserved IP</span></span>
```
PS C:\> New-AzureReservedIP -ReservedIPName $Name -Label $Label -Location $Location
```

<span data-ttu-id="bfbe0-112">이 명령은 웹, 작업자, 가상 컴퓨터를 포함 하는 클라우드 서비스를 만드는 데 사용할 수 있는 구독에 새 예약 된 IP 주소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-112">This command creates a new reserved IP address in the subscription, which can be used for creating cloud services that include Web, Worker, and Virtual Machines.</span></span>

### <span data-ttu-id="bfbe0-113">예제 2: 기존 IP를 기반으로 하는 예약 된 IP 만들기</span><span class="sxs-lookup"><span data-stu-id="bfbe0-113">Example 2: Create a reserved IP based on an existing IP</span></span>
```
PS C:\> New-AzureReservedIP -ReservedIPName resip14 -Location "West Europe" -ServiceName piptestwesteurope
```

<span data-ttu-id="bfbe0-114">이 명령은 지정 된 서비스에 대 한 기존 VIP (가상 IP)를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-114">This command creates an existing VIP (Virtual IP) on the specified service.</span></span>

## <span data-ttu-id="bfbe0-115">변수</span><span class="sxs-lookup"><span data-stu-id="bfbe0-115">PARAMETERS</span></span>

### <span data-ttu-id="bfbe0-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="bfbe0-116">-InformationAction</span></span>
<span data-ttu-id="bfbe0-117">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="bfbe0-118">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bfbe0-119">하기로</span><span class="sxs-lookup"><span data-stu-id="bfbe0-119">Continue</span></span>
- <span data-ttu-id="bfbe0-120">숨기기</span><span class="sxs-lookup"><span data-stu-id="bfbe0-120">Ignore</span></span>
- <span data-ttu-id="bfbe0-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="bfbe0-121">Inquire</span></span>
- <span data-ttu-id="bfbe0-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bfbe0-122">SilentlyContinue</span></span>
- <span data-ttu-id="bfbe0-123">중지가</span><span class="sxs-lookup"><span data-stu-id="bfbe0-123">Stop</span></span>
- <span data-ttu-id="bfbe0-124">대기</span><span class="sxs-lookup"><span data-stu-id="bfbe0-124">Suspend</span></span>

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

### <span data-ttu-id="bfbe0-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bfbe0-125">-InformationVariable</span></span>
<span data-ttu-id="bfbe0-126">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bfbe0-127">-레이블</span><span class="sxs-lookup"><span data-stu-id="bfbe0-127">-Label</span></span>
<span data-ttu-id="bfbe0-128">예약 된 IP 주소에 대 한 레이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-128">Specifies a label for the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfbe0-129">-위치</span><span class="sxs-lookup"><span data-stu-id="bfbe0-129">-Location</span></span>
<span data-ttu-id="bfbe0-130">예약 된 IP 주소를 만들 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-130">Specifies a location at which to create the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfbe0-131">-프로필</span><span class="sxs-lookup"><span data-stu-id="bfbe0-131">-Profile</span></span>
<span data-ttu-id="bfbe0-132">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bfbe0-133">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bfbe0-134">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="bfbe0-134">-ReservedIPName</span></span>
<span data-ttu-id="bfbe0-135">예약 된 IP 주소 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-135">Specifies the reserved IP address name.</span></span>

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

### <span data-ttu-id="bfbe0-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="bfbe0-136">-ServiceName</span></span>
<span data-ttu-id="bfbe0-137">서비스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-137">Specifies a service name.</span></span>

```yaml
Type: String
Parameter Sets: CreateInUseReservedIP
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfbe0-138">-슬롯</span><span class="sxs-lookup"><span data-stu-id="bfbe0-138">-Slot</span></span>
<span data-ttu-id="bfbe0-139">배포 슬롯을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-139">Specifies the deployment slot.</span></span>
<span data-ttu-id="bfbe0-140">이 매개 변수에 허용 되는 값은 Staging, 프로덕션입니다.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-140">The acceptable values for this parameter are: Staging, Production.</span></span>

```yaml
Type: String
Parameter Sets: CreateInUseReservedIP
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfbe0-141">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="bfbe0-141">-VirtualIPName</span></span>
<span data-ttu-id="bfbe0-142">이 cmdlet이 **VirtualIPName** 매개 변수를 사용 하 여 배포의 기존 VIP (가상 IP address)를 예약 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-142">Specifies that this cmdlet uses the **VirtualIPName** parameter to reserve an existing virtual IP address (VIP) in your deployment.</span></span>
<span data-ttu-id="bfbe0-143">이 매개 변수를 지정 하지 않으면이 cmdlet은 새 VIP를 예약 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-143">If this parameter is not specified, this cmdlet reserves a new VIP.</span></span>

```yaml
Type: String
Parameter Sets: CreateInUseReservedIP
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfbe0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfbe0-144">CommonParameters</span></span>
<span data-ttu-id="bfbe0-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfbe0-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfbe0-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfbe0-147">입력</span><span class="sxs-lookup"><span data-stu-id="bfbe0-147">INPUTS</span></span>

## <span data-ttu-id="bfbe0-148">출력</span><span class="sxs-lookup"><span data-stu-id="bfbe0-148">OUTPUTS</span></span>

## <span data-ttu-id="bfbe0-149">상속자</span><span class="sxs-lookup"><span data-stu-id="bfbe0-149">NOTES</span></span>

## <span data-ttu-id="bfbe0-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bfbe0-150">RELATED LINKS</span></span>

[<span data-ttu-id="bfbe0-151">Get-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="bfbe0-151">Get-AzureReservedIP</span></span>](./Get-AzureReservedIP.md)

[<span data-ttu-id="bfbe0-152">제거-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="bfbe0-152">Remove-AzureReservedIP</span></span>](./Remove-AzureReservedIP.md)


