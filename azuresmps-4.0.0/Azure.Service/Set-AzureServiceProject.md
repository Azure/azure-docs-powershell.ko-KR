---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D0A2B454-7BFF-4D4D-8A85-FDB47249758F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f4d1598f17629d178e1feff1b5549631be48c60
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045819"
---
# <span data-ttu-id="136f3-101">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="136f3-101">Set-AzureServiceProject</span></span>

## <span data-ttu-id="136f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="136f3-102">SYNOPSIS</span></span>
<span data-ttu-id="136f3-103">현재 서비스의 기본 위치, 구독, 슬롯 및 저장소 계정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="136f3-103">Sets default location, subscription, slot, and storage account for the current service.</span></span>

## <span data-ttu-id="136f3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="136f3-104">SYNTAX</span></span>

```
Set-AzureServiceProject [-Location <String>] [-Slot <String>] [-Storage <String>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="136f3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="136f3-105">DESCRIPTION</span></span>
<span data-ttu-id="136f3-106">**Set-AzureServiceProject** cmdlet은 현재 서비스에 대 한 배포 위치, 슬롯, 저장소 계정 및 구독을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="136f3-106">The **Set-AzureServiceProject** cmdlet sets the deployment location, slot, storage account, and subscription for the current service.</span></span>
<span data-ttu-id="136f3-107">이러한 값은 서비스를 클라우드에 게시할 때마다 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="136f3-107">These values are used whenever the service is published to the cloud.</span></span>

## <span data-ttu-id="136f3-108">예제의</span><span class="sxs-lookup"><span data-stu-id="136f3-108">EXAMPLES</span></span>

### <span data-ttu-id="136f3-109">예제 1: 기본 설정</span><span class="sxs-lookup"><span data-stu-id="136f3-109">Example 1: Basic settings</span></span>
```
PS C:\> Set-AzureServiceProject -Location "North Central US" -Slot Production -Storage myStorageAccount -Subscription myAzureSubscription
```

<span data-ttu-id="136f3-110">서비스의 배포 위치를 북쪽 중부 US 지역으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="136f3-110">Sets the deployment location for the service to the North Central US region.</span></span>
<span data-ttu-id="136f3-111">배포 슬롯을 프로덕션으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="136f3-111">Sets the deployment slot to Production.</span></span> <span data-ttu-id="136f3-112">MyStorageAccount에 대 한 서비스 정의를 준비 하는 데 사용할 저장소 계정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="136f3-112">Sets the storage account that will be used to stage the service definition to myStorageAccount.</span></span>
<span data-ttu-id="136f3-113">서비스를 mySubscription에 호스팅할 구독을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="136f3-113">Sets the subscription that will host the service to mySubscription.</span></span>
<span data-ttu-id="136f3-114">서비스를 클라우드에 게시할 때마다 해당 서비스가 북미 중앙 미국 지역의 데이터 센터에서 호스팅되므로 배포 슬롯이 업데이트 되며 지정 된 구독 및 저장소 계정이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="136f3-114">Whenever the service is published to the cloud, it will be hosted in a data center in the North Central US region, it will update the deployment slot, and it will use the specified subscription and storage account.</span></span>

## <span data-ttu-id="136f3-115">변수</span><span class="sxs-lookup"><span data-stu-id="136f3-115">PARAMETERS</span></span>

### <span data-ttu-id="136f3-116">-위치</span><span class="sxs-lookup"><span data-stu-id="136f3-116">-Location</span></span>
<span data-ttu-id="136f3-117">서비스를 호스팅할 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="136f3-117">The region in which the service will be hosted.</span></span>
<span data-ttu-id="136f3-118">서비스를 클라우드에 게시할 때마다이 값이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="136f3-118">This value is used whenever the service is published to the cloud.</span></span>
<span data-ttu-id="136f3-119">가능한 값은 어디에서 든 아시아, 어디서 나 유럽, 어디서 나 미국, 동쪽 미국, 북부 중앙 미국, 동유럽, 남 중앙 미국, 동남 아시아, 서유럽, 서쪽 미국입니다.</span><span class="sxs-lookup"><span data-stu-id="136f3-119">Possible values are: Anywhere Asia, Anywhere Europe, Anywhere US, East Asia, East US, North Central US, North Europe, South Central US, Southeast Asia, West Europe, West US.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="136f3-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="136f3-120">-PassThru</span></span>
<span data-ttu-id="136f3-121">이 cmdlet이 작동 하는 항목을 나타내는 개체를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="136f3-121">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="136f3-122">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="136f3-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="136f3-123">-프로필</span><span class="sxs-lookup"><span data-stu-id="136f3-123">-Profile</span></span>
<span data-ttu-id="136f3-124">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="136f3-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="136f3-125">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="136f3-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="136f3-126">-슬롯</span><span class="sxs-lookup"><span data-stu-id="136f3-126">-Slot</span></span>
<span data-ttu-id="136f3-127">서비스를 호스트할 슬롯 (제작 또는 준비)입니다.</span><span class="sxs-lookup"><span data-stu-id="136f3-127">The slot (production or staging) in which the service will be hosted.</span></span>
<span data-ttu-id="136f3-128">서비스를 클라우드에 게시할 때마다이 값이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="136f3-128">This value is used whenever the service is published to the cloud.</span></span>
<span data-ttu-id="136f3-129">사용할 수 있는 값은 프로덕션, 준비입니다.</span><span class="sxs-lookup"><span data-stu-id="136f3-129">Possible values are: Production, Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="136f3-130">-저장소</span><span class="sxs-lookup"><span data-stu-id="136f3-130">-Storage</span></span>
<span data-ttu-id="136f3-131">클라우드에 서비스 패키지를 업로드할 때 사용할 저장소 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="136f3-131">The storage account to be used when uploading the service package to the cloud.</span></span>
<span data-ttu-id="136f3-132">저장소 계정이 없는 경우 서비스를 클라우드에 게시할 때 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="136f3-132">If the storage account doesn't exist, it will be created when the service is published to the cloud.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="136f3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="136f3-133">CommonParameters</span></span>
<span data-ttu-id="136f3-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="136f3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="136f3-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="136f3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="136f3-136">입력</span><span class="sxs-lookup"><span data-stu-id="136f3-136">INPUTS</span></span>

## <span data-ttu-id="136f3-137">출력</span><span class="sxs-lookup"><span data-stu-id="136f3-137">OUTPUTS</span></span>

## <span data-ttu-id="136f3-138">상속자</span><span class="sxs-lookup"><span data-stu-id="136f3-138">NOTES</span></span>
* <span data-ttu-id="136f3-139">노드 개발자, php-개발자, python-개발자</span><span class="sxs-lookup"><span data-stu-id="136f3-139">node-dev, php-dev, python-dev</span></span>

## <span data-ttu-id="136f3-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="136f3-140">RELATED LINKS</span></span>

[<span data-ttu-id="136f3-141">새-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="136f3-141">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)

[<span data-ttu-id="136f3-142">게시-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="136f3-142">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="136f3-143">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="136f3-143">Set-AzureServiceProjectRole</span></span>](./Set-AzureServiceProjectRole.md)


