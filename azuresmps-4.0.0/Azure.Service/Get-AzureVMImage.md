---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E712421A-FA69-46E7-A0DE-F2734D767F2D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8355e0a1d36a6c1dc5b2ca8172cde5bf94480bbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046532"
---
# <span data-ttu-id="ec0e7-101">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="ec0e7-101">Get-AzureVMImage</span></span>

## <span data-ttu-id="ec0e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec0e7-102">SYNOPSIS</span></span>
<span data-ttu-id="ec0e7-103">하나 또는 여러 운영 체제 목록 또는 이미지 리포지토리의 가상 컴퓨터 이미지에 대 한 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ec0e7-103">Gets the properties on one or a list of operating systems or a virtual machine image in the image repository.</span></span>

## <span data-ttu-id="ec0e7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ec0e7-104">SYNTAX</span></span>

```
Get-AzureVMImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ec0e7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ec0e7-105">DESCRIPTION</span></span>
<span data-ttu-id="ec0e7-106">**AzureVMImage** cmdlet은 하나 또는 여러 운영 체제 또는 이미지 리포지토리의 가상 컴퓨터 이미지 목록에 대 한 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ec0e7-106">The **Get-AzureVMImage** cmdlet gets properties on one or a list of operating systems or a virtual machine image in the image repository.</span></span>
<span data-ttu-id="ec0e7-107">Cmdlet은 리포지토리의 모든 이미지에 대 한 정보를 반환 하거나, 해당 이미지 이름을 제공 하는 경우 특정 이미지에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec0e7-107">The cmdlet returns information for all images in the repository, or about a specific image if its image name is provided.</span></span>

## <span data-ttu-id="ec0e7-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ec0e7-108">EXAMPLES</span></span>

### <span data-ttu-id="ec0e7-109">예제 1: 현재 이미지 리포지토리에서 특정 이미지 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ec0e7-109">Example 1: Get a specific image object from the current image repository.</span></span>
```
PS C:\> Get-AzureVMImage -ImageName Image001
```

<span data-ttu-id="ec0e7-110">이 명령은 현재 이미지 리포지토리에서 Image001 이라는 이미지 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ec0e7-110">This command gets the image object named Image001 from the current image repository.</span></span>

### <span data-ttu-id="ec0e7-111">예제 2: 현재 이미지 리포지토리에서 모든 이미지 가져오기</span><span class="sxs-lookup"><span data-stu-id="ec0e7-111">Example 2: Get all images from the current image repository</span></span>
```
PS C:\> Get-AzureVMImage
```

<span data-ttu-id="ec0e7-112">이 명령은 현재 이미지 리포지토리에서 모든 이미지를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec0e7-112">This command retrieves all the images from the current image repository.</span></span>

### <span data-ttu-id="ec0e7-113">예제 3: 구독 컨텍스트를 설정한 다음 모든 이미지 가져오기</span><span class="sxs-lookup"><span data-stu-id="ec0e7-113">Example 3: Set the subscription context and then get all the images</span></span>
```
PS C:\> $SubsId = <MySubscriptionID>
C:\PS>$Cert = Get-AzureCertificate cert:\LocalMachine\MY\<CertificateThumbprint>
C:\PS>$MyOSImages = Get-AzureVMImage
```

<span data-ttu-id="ec0e7-114">이 명령은 구독 컨텍스트를 설정한 다음 이미지 리포지토리에서 모든 이미지를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec0e7-114">This command sets the subscription context and then retrieves all the images from the image repository.</span></span>

## <span data-ttu-id="ec0e7-115">변수</span><span class="sxs-lookup"><span data-stu-id="ec0e7-115">PARAMETERS</span></span>

### <span data-ttu-id="ec0e7-116">-ImageName</span><span class="sxs-lookup"><span data-stu-id="ec0e7-116">-ImageName</span></span>
<span data-ttu-id="ec0e7-117">이미지 리포지토리에서 운영 체제 또는 가상 컴퓨터 이미지의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec0e7-117">Specifies the name of the operating system or virtual machine image in the image repository.</span></span>
<span data-ttu-id="ec0e7-118">이 매개 변수를 지정 하지 않으면 모든 이미지가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec0e7-118">If you do not specify this parameter, all the images are returned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec0e7-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ec0e7-119">-InformationAction</span></span>
<span data-ttu-id="ec0e7-120">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec0e7-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ec0e7-121">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ec0e7-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ec0e7-122">하기로</span><span class="sxs-lookup"><span data-stu-id="ec0e7-122">Continue</span></span>
- <span data-ttu-id="ec0e7-123">숨기기</span><span class="sxs-lookup"><span data-stu-id="ec0e7-123">Ignore</span></span>
- <span data-ttu-id="ec0e7-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="ec0e7-124">Inquire</span></span>
- <span data-ttu-id="ec0e7-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ec0e7-125">SilentlyContinue</span></span>
- <span data-ttu-id="ec0e7-126">중지가</span><span class="sxs-lookup"><span data-stu-id="ec0e7-126">Stop</span></span>
- <span data-ttu-id="ec0e7-127">대기</span><span class="sxs-lookup"><span data-stu-id="ec0e7-127">Suspend</span></span>

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

### <span data-ttu-id="ec0e7-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ec0e7-128">-InformationVariable</span></span>
<span data-ttu-id="ec0e7-129">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec0e7-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ec0e7-130">-프로필</span><span class="sxs-lookup"><span data-stu-id="ec0e7-130">-Profile</span></span>
<span data-ttu-id="ec0e7-131">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec0e7-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ec0e7-132">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="ec0e7-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ec0e7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec0e7-133">CommonParameters</span></span>
<span data-ttu-id="ec0e7-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec0e7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec0e7-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec0e7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec0e7-136">입력</span><span class="sxs-lookup"><span data-stu-id="ec0e7-136">INPUTS</span></span>

## <span data-ttu-id="ec0e7-137">출력</span><span class="sxs-lookup"><span data-stu-id="ec0e7-137">OUTPUTS</span></span>

## <span data-ttu-id="ec0e7-138">상속자</span><span class="sxs-lookup"><span data-stu-id="ec0e7-138">NOTES</span></span>

## <span data-ttu-id="ec0e7-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec0e7-139">RELATED LINKS</span></span>

[<span data-ttu-id="ec0e7-140">추가-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="ec0e7-140">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="ec0e7-141">제거-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="ec0e7-141">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="ec0e7-142">저장-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="ec0e7-142">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="ec0e7-143">업데이트-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="ec0e7-143">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


