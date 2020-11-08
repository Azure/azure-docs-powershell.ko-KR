---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 482E8CD6-C38F-4BD5-8214-016D0D8C7FD0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6381b8e0fac5ebf047122f131af6087d5bb5a9fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045554"
---
# <span data-ttu-id="86515-101">Get-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="86515-101">Get-AzureStorSimpleResource</span></span>

## <span data-ttu-id="86515-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86515-102">SYNOPSIS</span></span>
<span data-ttu-id="86515-103">만든 모든 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="86515-103">Gets all resources that you created.</span></span>

## <span data-ttu-id="86515-104">구문과</span><span class="sxs-lookup"><span data-stu-id="86515-104">SYNTAX</span></span>

```
Get-AzureStorSimpleResource [-ResourceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="86515-105">설명은</span><span class="sxs-lookup"><span data-stu-id="86515-105">DESCRIPTION</span></span>
<span data-ttu-id="86515-106">**Get-AzureStorSimpleResource** Cmdlet는 Azure 포털을 사용 하 여 만든 모든 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="86515-106">The **Get-AzureStorSimpleResource** cmdlet gets all resources that you created by using Azure Portal.</span></span>
<span data-ttu-id="86515-107">Cmdlet은 리소스에 연결 하는 데 사용할 수 있는 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="86515-107">The cmdlet gets details you can use to connect to the resources.</span></span>

## <span data-ttu-id="86515-108">예제의</span><span class="sxs-lookup"><span data-stu-id="86515-108">EXAMPLES</span></span>

### <span data-ttu-id="86515-109">예제 1: 모든 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="86515-109">Example 1: Get all resources</span></span>
```
PS C:\>Get-AzureStorSimpleResource
VERBOSE: ClientRequestId: 5cd61b91-ef40-43b4-986d-156e06d2ed65_PS

ResourceName                                      ResourceId           ResourceState
------------                                      ----------           -------------
Contoso63-Tsqa                                    8838459798595306468  Started
Contoso68-Tsqa                                    2859070203638134681  Started
Contoso73-Tsqa                                    7871392677286863733  Started
Contoso87-Tsqa                                    1909806764156522689  Started
VERBOSE: Found 4 StorSimple resources.
```

<span data-ttu-id="86515-110">이 명령은 만든 모든 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="86515-110">This command gets all the resources you created.</span></span>
<span data-ttu-id="86515-111">이 예제에는 세 개의 리소스가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="86515-111">In this example, there are three resources.</span></span>

### <span data-ttu-id="86515-112">예제 2: 이름을 사용 하 여 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="86515-112">Example 2: Get a resource by using its name</span></span>
```
PS C:\>Get-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa"
VERBOSE: ClientRequestId: efc3c85c-12aa-4345-b6eb-ccc532de4825_PS

ResourceName                                      ResourceId           ResourceState
------------                                      ----------           -------------
Contoso63-Tsqa                                    1909806764156522689  Started
VERBOSE: Found 1 StorSimple resource.
```

<span data-ttu-id="86515-113">이 명령은 Contoso63 라는 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="86515-113">This command gets the resource named Contoso63-Tsqa.</span></span>

### <span data-ttu-id="86515-114">예제 3: 존재 하지 않는 리소스 가져오기 시도</span><span class="sxs-lookup"><span data-stu-id="86515-114">Example 3: Attempt to get a nonexistent resource</span></span>
```
PS C:\>Get-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
VERBOSE: ClientRequestId: 5d08d40b-f9d7-4d43-956f-13f01e89625b_PS
VERBOSE: Invalid input : Could not find a resource named Contoso64-Tsqa in your subscription.
```

<span data-ttu-id="86515-115">이 명령은 Contoso64 라는 리소스를 가져오려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="86515-115">This command attempts to get the resource named Contoso64-Tsqa.</span></span>
<span data-ttu-id="86515-116">이 이름을 가진 리소스가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="86515-116">There is no resource that has this name.</span></span>
<span data-ttu-id="86515-117">이 예제는 리소스를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="86515-117">This example does not return any resource.</span></span>

## <span data-ttu-id="86515-118">변수</span><span class="sxs-lookup"><span data-stu-id="86515-118">PARAMETERS</span></span>

### <span data-ttu-id="86515-119">-프로필</span><span class="sxs-lookup"><span data-stu-id="86515-119">-Profile</span></span>
<span data-ttu-id="86515-120">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86515-120">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="86515-121">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="86515-121">-ResourceName</span></span>
<span data-ttu-id="86515-122">이 cmdlet이 가져오는 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86515-122">Specifies the name of the resource that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86515-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86515-123">CommonParameters</span></span>
<span data-ttu-id="86515-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="86515-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86515-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86515-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86515-126">입력</span><span class="sxs-lookup"><span data-stu-id="86515-126">INPUTS</span></span>

### <span data-ttu-id="86515-127">않아야</span><span class="sxs-lookup"><span data-stu-id="86515-127">None</span></span>

## <span data-ttu-id="86515-128">출력</span><span class="sxs-lookup"><span data-stu-id="86515-128">OUTPUTS</span></span>

### <span data-ttu-id="86515-129">IEnumerable \<ResourceCredentials\> , ResourceCredentials</span><span class="sxs-lookup"><span data-stu-id="86515-129">IEnumerable\<ResourceCredentials\>, ResourceCredentials</span></span>
<span data-ttu-id="86515-130">이 cmdlet은 다음 속성을 포함 하는 **ResourceCredentials** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="86515-130">This cmdlet returns **ResourceCredentials** objects that contain the following properties:</span></span> 

- <span data-ttu-id="86515-131">**Context.resourcename**</span><span class="sxs-lookup"><span data-stu-id="86515-131">**ResourceName**</span></span>
- <span data-ttu-id="86515-132">**ResouceId**</span><span class="sxs-lookup"><span data-stu-id="86515-132">**ResouceId**</span></span>
- <span data-ttu-id="86515-133">**ResourceState**</span><span class="sxs-lookup"><span data-stu-id="86515-133">**ResourceState**</span></span>

## <span data-ttu-id="86515-134">상속자</span><span class="sxs-lookup"><span data-stu-id="86515-134">NOTES</span></span>

## <span data-ttu-id="86515-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="86515-135">RELATED LINKS</span></span>

[<span data-ttu-id="86515-136">Get-AzureStorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="86515-136">Get-AzureStorSimpleResourceContext</span></span>](./Get-AzureStorSimpleResourceContext.md)

[<span data-ttu-id="86515-137">선택-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="86515-137">Select-AzureStorSimpleResource</span></span>](./Select-AzureStorSimpleResource.md)


