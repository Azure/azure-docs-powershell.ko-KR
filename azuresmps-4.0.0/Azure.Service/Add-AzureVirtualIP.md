---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FBED8515-4216-4AB6-B34E-D14A6063A3A7
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2f145ec51bc6744d877661554e3d8e475d722fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045713"
---
# <span data-ttu-id="4b31b-101">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="4b31b-101">Add-AzureVirtualIP</span></span>

## <span data-ttu-id="4b31b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b31b-102">SYNOPSIS</span></span>
<span data-ttu-id="4b31b-103">클라우드 서비스에 가상 IP를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b31b-103">Adds a virtual IP to a cloud service.</span></span>

## <span data-ttu-id="4b31b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4b31b-104">SYNTAX</span></span>

```
Add-AzureVirtualIP [-ServiceName] <String> [-VirtualIPName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4b31b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4b31b-105">DESCRIPTION</span></span>
<span data-ttu-id="4b31b-106">**추가-AzureVirtualIP** Cmdlet은 Azure 서비스에 새 VIP (가상 IP)를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b31b-106">The **Add-AzureVirtualIP** cmdlet adds a new virtual IP (VIP) to your Azure service.</span></span>
<span data-ttu-id="4b31b-107">새 가상 IP에는 이름이 있지만 IP 주소는 할당 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4b31b-107">The new virtual IP has a name but is not allocated an IP address.</span></span>

<span data-ttu-id="4b31b-108">IP 주소는 끝점을 VIP에 연결 하는 경우에만 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b31b-108">The IP address is allocated only when you associate an endpoint to the VIP.</span></span>
<span data-ttu-id="4b31b-109">자세한 내용은 Add-AzureEndpoint을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4b31b-109">See Add-AzureEndpoint for more details.</span></span>

<span data-ttu-id="4b31b-110">끝점에 연결 된 경우에만 구독이 추가 Vip에 대해 부과 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b31b-110">Your subscription is charged for extra VIPs only once they are associated with an endpoint.</span></span>

## <span data-ttu-id="4b31b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="4b31b-111">EXAMPLES</span></span>

### <span data-ttu-id="4b31b-112">예제 1: 서비스에 가상 IP 추가</span><span class="sxs-lookup"><span data-stu-id="4b31b-112">Example 1: Add a virtual IP to a service</span></span>
```
PS C:\> Add-AzureVirtualIP -VirtualIPName "Vip01" -ServiceName "ContosoService03"
OperationDescription OperationId                          OperationStatus
-------------------- -----------                          ---------------
Add-AzureVirtualIP   4bd7b638-d2e7-216f-ba38-5221233d70ce Succeeded
```

<span data-ttu-id="4b31b-113">이 명령은 가상 IP 주소를 서비스에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b31b-113">This command adds a virtual IP address to a service.</span></span>

## <span data-ttu-id="4b31b-114">변수</span><span class="sxs-lookup"><span data-stu-id="4b31b-114">PARAMETERS</span></span>

### <span data-ttu-id="4b31b-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4b31b-115">-InformationAction</span></span>
<span data-ttu-id="4b31b-116">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b31b-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4b31b-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4b31b-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4b31b-118">하기로</span><span class="sxs-lookup"><span data-stu-id="4b31b-118">Continue</span></span>
- <span data-ttu-id="4b31b-119">숨기기</span><span class="sxs-lookup"><span data-stu-id="4b31b-119">Ignore</span></span>
- <span data-ttu-id="4b31b-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="4b31b-120">Inquire</span></span>
- <span data-ttu-id="4b31b-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4b31b-121">SilentlyContinue</span></span>
- <span data-ttu-id="4b31b-122">중지가</span><span class="sxs-lookup"><span data-stu-id="4b31b-122">Stop</span></span>
- <span data-ttu-id="4b31b-123">대기</span><span class="sxs-lookup"><span data-stu-id="4b31b-123">Suspend</span></span>

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

### <span data-ttu-id="4b31b-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4b31b-124">-InformationVariable</span></span>
<span data-ttu-id="4b31b-125">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b31b-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4b31b-126">-프로필</span><span class="sxs-lookup"><span data-stu-id="4b31b-126">-Profile</span></span>
<span data-ttu-id="4b31b-127">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b31b-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4b31b-128">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="4b31b-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4b31b-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4b31b-129">-ServiceName</span></span>
<span data-ttu-id="4b31b-130">서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b31b-130">Specifies the name of the service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b31b-131">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="4b31b-131">-VirtualIPName</span></span>
<span data-ttu-id="4b31b-132">가상 IP 주소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b31b-132">Specifies the name of the virtual IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b31b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b31b-133">CommonParameters</span></span>
<span data-ttu-id="4b31b-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b31b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b31b-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b31b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b31b-136">입력</span><span class="sxs-lookup"><span data-stu-id="4b31b-136">INPUTS</span></span>

## <span data-ttu-id="4b31b-137">출력</span><span class="sxs-lookup"><span data-stu-id="4b31b-137">OUTPUTS</span></span>

### <span data-ttu-id="4b31b-138">WindowsAzure. 유틸리티. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="4b31b-138">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="4b31b-139">상속자</span><span class="sxs-lookup"><span data-stu-id="4b31b-139">NOTES</span></span>

## <span data-ttu-id="4b31b-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b31b-140">RELATED LINKS</span></span>

[<span data-ttu-id="4b31b-141">추가-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b31b-141">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="4b31b-142">-AzureVirtualIP 제거</span><span class="sxs-lookup"><span data-stu-id="4b31b-142">Remove-AzureVirtualIP</span></span>](./Remove-AzureVirtualIP.md)


