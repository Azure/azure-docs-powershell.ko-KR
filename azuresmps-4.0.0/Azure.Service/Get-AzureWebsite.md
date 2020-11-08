---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E4B1AA31-1185-4035-86E6-2BB2587285C6
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8273613081ab6bab0c9c3481df90f5b680b3355
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046274"
---
# <span data-ttu-id="79ef1-101">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="79ef1-101">Get-AzureWebsite</span></span>

## <span data-ttu-id="79ef1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79ef1-102">SYNOPSIS</span></span>
<span data-ttu-id="79ef1-103">현재 구독에서 Azure 웹 사이트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-103">Gets Azure websites in the current subscription.</span></span>

## <span data-ttu-id="79ef1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="79ef1-104">SYNTAX</span></span>

```
Get-AzureWebsite [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="79ef1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="79ef1-105">DESCRIPTION</span></span>
<span data-ttu-id="79ef1-106">**AzureWebsite** cmdlet은 현재 구독의 Azure websites에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-106">The **Get-AzureWebsite** cmdlet gets information about Azure websites in the current subscription.</span></span>

<span data-ttu-id="79ef1-107">기본적으로 **Get-AzureWebsite** 는 현재 구독의 모든 Azure 웹 사이트를 가져오며 사이트에 대 한 기본 정보를 제공 하는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-107">By default, **Get-AzureWebsite** gets all Azure websites in the current subscription and returns an object that provides basic information about the sites.</span></span>
<span data-ttu-id="79ef1-108">*Name* 매개 변수를 사용 하는 경우 **Get-AzureWebsite** 는 구성 세부 정보를 포함 하 여 자세한 정보가 포함 된 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-108">When you use the *Name* parameter, **Get-AzureWebsite** returns an object with extensive information, including configuration details.</span></span>

<span data-ttu-id="79ef1-109">현재 구독은 "current"로 지정 된 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-109">The current subscription is the subscription that is designated as "current."</span></span> <span data-ttu-id="79ef1-110">현재 구독을 찾으려면 [Get-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397623) Cmdlet의 *현재* 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-110">To find the current subscription, use the *Current* parameter of the [Get-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397623) cmdlet.</span></span>
<span data-ttu-id="79ef1-111">현재 구독을 변경 하려면 [Select-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397628) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-111">To change the current subscription, use the [Select-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397628) cmdlet.</span></span>

<span data-ttu-id="79ef1-112">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-112">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="79ef1-113">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-113">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="79ef1-114">예제의</span><span class="sxs-lookup"><span data-stu-id="79ef1-114">EXAMPLES</span></span>

### <span data-ttu-id="79ef1-115">예제 1: 구독에 있는 모든 웹 사이트 가져오기</span><span class="sxs-lookup"><span data-stu-id="79ef1-115">Example 1: Get all websites in the subscription</span></span>
```
PS C:\> Get-AzureWebsite
```

<span data-ttu-id="79ef1-116">이 명령은 현재 구독에 있는 모든 Azure 웹 사이트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-116">This command gets all Azure websites in the current subscription.</span></span>

### <span data-ttu-id="79ef1-117">예제 2: 이름으로 웹 사이트 가져오기</span><span class="sxs-lookup"><span data-stu-id="79ef1-117">Example 2: Get a website by name</span></span>
```
PS C:\> Get-AzureWebsite -Name ContosoWeb
```

<span data-ttu-id="79ef1-118">이 명령은 구성 정보를 포함 하 여 ContosoWeb Azure 웹 사이트에 대 한 자세한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-118">This command gets detailed information about the ContosoWeb Azure website, including configuration information.</span></span>
<span data-ttu-id="79ef1-119">*Name* 매개 변수를 사용 하는 경우 **Get-AzureWebsite** 는 웹 사이트에 대 한 확장 정보가 있는 **sitewithconfig** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-119">When you use the *Name* parameter, **Get-AzureWebsite** returns a **SiteWithConfig** object with extended information about the website.</span></span>

### <span data-ttu-id="79ef1-120">예제 3: 모든 웹사이트에 대 한 자세한 정보 보기</span><span class="sxs-lookup"><span data-stu-id="79ef1-120">Example 3: Get detailed information about all websites</span></span>
```
PS C:\> Get-AzureWebsite | ForEach-Object {Get-AzureWebsite -Name $_.Name}
```

<span data-ttu-id="79ef1-121">이 명령은 구독의 모든 웹사이트에 대 한 자세한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-121">This command gets detailed information about all websites in the subscription.</span></span>
<span data-ttu-id="79ef1-122">**AzureWebsite** 명령을 사용 하 여 모든 웹 사이트를 가져와 **ForEach-개체** cmdlet을 사용 하 여 각 웹 사이트를 이름으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-122">It uses a **Get-AzureWebsite** command to get all websites and then uses the **ForEach-Object** cmdlet to get each website by name.</span></span>

### <span data-ttu-id="79ef1-123">예제 4: 배포 슬롯에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="79ef1-123">Example 4: Get information about a deployment slot</span></span>
```
PS C:\> Get-AzureWebsite -Name ContosoWeb -Slot Staging
```

<span data-ttu-id="79ef1-124">이 명령은 ContosoWeb 웹 사이트의 스테이징 배포 슬롯을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-124">This command gets the Staging deployment slot of the ContosoWeb website.</span></span>
<span data-ttu-id="79ef1-125">배포 슬롯을 사용 하면 다른 버전의 Azure 웹 사이트를 공개 하지 않고 테스트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-125">Deployment slots let you test different versions of your Azure website without releasing them to the public.</span></span>

### <span data-ttu-id="79ef1-126">예제 5: 웹 사이트 인스턴스 가져오기</span><span class="sxs-lookup"><span data-stu-id="79ef1-126">Example 5: Get website instances</span></span>
```
PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances

InstanceId
----------
2d8e712fb8f85d061c30fd793a534e6700a175f9a9ab12ca55cb3b0edfcc10ee
5834916b8cef49249b18187708223a33fbbc4352d33b48369f3166644bdd3445

PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances.Count
2
```

<span data-ttu-id="79ef1-127">이 예제의 명령은 Azure 웹 사이트의 Instances 속성을 사용 하 여 현재 실행 중인 웹 사이트 인스턴스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-127">The commands in this example use the Instances property of an Azure website to get information about currently running website instances.</span></span>
<span data-ttu-id="79ef1-128">**인스턴스** 속성은 Azure 모듈 버전 0.8.3의 **sitewithconfig** 개체에 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-128">The **Instances** property was added to the **SiteWithConfig** object in version 0.8.3 of the Azure module.</span></span>

<span data-ttu-id="79ef1-129">첫 번째 명령은 현재 웹 사이트에서 실행 중인 모든 인스턴스의 인스턴스 Id를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-129">The first command gets the instance IDs of all currently running instances of a website.</span></span>
<span data-ttu-id="79ef1-130">두 번째 명령은 웹 사이트의 실행 중인 인스턴스 수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-130">The second command gets the number of running instances of the website.</span></span>
<span data-ttu-id="79ef1-131">모든 배열에서 **Count** 속성을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-131">You can use the **Count** property on any array.</span></span>

## <span data-ttu-id="79ef1-132">변수</span><span class="sxs-lookup"><span data-stu-id="79ef1-132">PARAMETERS</span></span>

### <span data-ttu-id="79ef1-133">-이름</span><span class="sxs-lookup"><span data-stu-id="79ef1-133">-Name</span></span>
<span data-ttu-id="79ef1-134">지정 된 웹 사이트에 대 한 자세한 구성 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-134">Gets detailed configuration information about the specified website.</span></span>
<span data-ttu-id="79ef1-135">구독에 한 웹 사이트의 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-135">Enter the name of one website in the subscription.</span></span>
<span data-ttu-id="79ef1-136">기본적으로 **Get-AzureWebsite** 는 현재 구독에 있는 모든 웹 사이트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-136">By default, **Get-AzureWebsite** gets all websites in the current subscription.</span></span>
<span data-ttu-id="79ef1-137">*Name* 값은 와일드 카드 문자를 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-137">The *Name* value does not support wildcard characters.</span></span>

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

### <span data-ttu-id="79ef1-138">-프로필</span><span class="sxs-lookup"><span data-stu-id="79ef1-138">-Profile</span></span>
<span data-ttu-id="79ef1-139">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="79ef1-140">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="79ef1-141">-슬롯</span><span class="sxs-lookup"><span data-stu-id="79ef1-141">-Slot</span></span>
<span data-ttu-id="79ef1-142">웹 사이트의 지정 된 배포 슬롯을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-142">Gets the specified deployment slot of the website.</span></span>
<span data-ttu-id="79ef1-143">슬롯 이름 (예: "준비" 또는 "생산")을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-143">Enter the slot name, such as "Staging" or "Production".</span></span>
<span data-ttu-id="79ef1-144">배포 슬롯에 대 한 자세한 내용은 Microsoft Azure 웹 사이트의 단계적 배포를 참조 https://azure.microsoft.com/en-us/documentation/articles/web-sites-staged-publishing/ 하세요.</span><span class="sxs-lookup"><span data-stu-id="79ef1-144">For more information about deployment slots, see Staged Deployment on Microsoft Azure Web Siteshttps://azure.microsoft.com/en-us/documentation/articles/web-sites-staged-publishing/.</span></span>
<span data-ttu-id="79ef1-145">기존 Azure 웹 사이트에 배포 슬롯을 추가 하려면 Set-AzureWebsite cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-145">To add a deployment slot to an existing Azure website, use the Set-AzureWebsite cmdlet.</span></span>

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

### <span data-ttu-id="79ef1-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79ef1-146">CommonParameters</span></span>
<span data-ttu-id="79ef1-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79ef1-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79ef1-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79ef1-149">입력</span><span class="sxs-lookup"><span data-stu-id="79ef1-149">INPUTS</span></span>

### <span data-ttu-id="79ef1-150">않아야</span><span class="sxs-lookup"><span data-stu-id="79ef1-150">None</span></span>
<span data-ttu-id="79ef1-151">속성 이름으로이 cmdlet에 대 한 입력을 파이프로 지정할 수 있지만 값을 기준으로 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-151">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="79ef1-152">출력</span><span class="sxs-lookup"><span data-stu-id="79ef1-152">OUTPUTS</span></span>

### <span data-ttu-id="79ef1-153">WindowsAzure. \*. \* WebEntities. Site</span><span class="sxs-lookup"><span data-stu-id="79ef1-153">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.Site</span></span>
<span data-ttu-id="79ef1-154">기본적으로 **Get-AzureWebsite** 는 **사이트** 개체의 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-154">By default, **Get-AzureWebsite** returns an array of **Site** objects.</span></span>

### <span data-ttu-id="79ef1-155">WindowsAzure. 유틸리티. a i m/WebEntities. SiteWithConfig</span><span class="sxs-lookup"><span data-stu-id="79ef1-155">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.SiteWithConfig</span></span>
<span data-ttu-id="79ef1-156">*Name* 매개 변수를 사용 하는 경우 **Get-AzureWebsite** 는 **sitewithconfig** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="79ef1-156">When you use the *Name* parameter, **Get-AzureWebsite** returns a **SiteWithConfig** object.</span></span>

## <span data-ttu-id="79ef1-157">상속자</span><span class="sxs-lookup"><span data-stu-id="79ef1-157">NOTES</span></span>

## <span data-ttu-id="79ef1-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="79ef1-158">RELATED LINKS</span></span>

[<span data-ttu-id="79ef1-159">새로운 AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="79ef1-159">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="79ef1-160">제거-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="79ef1-160">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="79ef1-161">시작-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="79ef1-161">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="79ef1-162">중지-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="79ef1-162">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)

[<span data-ttu-id="79ef1-163">쇼-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="79ef1-163">Show-AzureWebsite</span></span>](./Show-AzureWebsite.md)


