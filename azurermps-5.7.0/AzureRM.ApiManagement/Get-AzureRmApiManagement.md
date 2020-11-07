---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
ms.openlocfilehash: 50a548716019f3b5e80cde4b89ae666f5b6199ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711216"
---
# <span data-ttu-id="87928-101">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="87928-101">Get-AzureRmApiManagement</span></span>

## <span data-ttu-id="87928-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87928-102">SYNOPSIS</span></span>
<span data-ttu-id="87928-103">목록 또는 특정 API 관리 서비스 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="87928-103">Gets a list or a particular API Management Service description.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87928-104">구문과</span><span class="sxs-lookup"><span data-stu-id="87928-104">SYNTAX</span></span>

### <span data-ttu-id="87928-105">GetBySubscription (기본값)</span><span class="sxs-lookup"><span data-stu-id="87928-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87928-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="87928-106">GetByResourceGroup</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="87928-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="87928-107">GetByResource</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87928-108">설명은</span><span class="sxs-lookup"><span data-stu-id="87928-108">DESCRIPTION</span></span>
<span data-ttu-id="87928-109">**AzureRmApiManagement** cmdlet은 구독 또는 지정 된 리소스 그룹 또는 특정 API management 아래에 있는 모든 API management 서비스의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="87928-109">The **Get-AzureRmApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="87928-110">예제의</span><span class="sxs-lookup"><span data-stu-id="87928-110">EXAMPLES</span></span>

### <span data-ttu-id="87928-111">예제 1: 모든 API Management 서비스 가져오기</span><span class="sxs-lookup"><span data-stu-id="87928-111">Example 1: Get all API Management services</span></span>
```
PS C:\>Get-AzureRmApiManagement
```

<span data-ttu-id="87928-112">이 명령은 구독 내의 모든 API Management 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="87928-112">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="87928-113">예제 2: 모든 API Management 서비스를 특정 이름으로 가져오기</span><span class="sxs-lookup"><span data-stu-id="87928-113">Example 2: Get all API Management services by a specific name</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="87928-114">이 명령은 모든 API Management 서비스를 이름별로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="87928-114">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="87928-115">변수</span><span class="sxs-lookup"><span data-stu-id="87928-115">PARAMETERS</span></span>

### <span data-ttu-id="87928-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87928-116">-DefaultProfile</span></span>
<span data-ttu-id="87928-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="87928-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87928-118">-이름</span><span class="sxs-lookup"><span data-stu-id="87928-118">-Name</span></span>
<span data-ttu-id="87928-119">API Management 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87928-119">Specifies the name of API Management service.</span></span>

```yaml
Type: String
Parameter Sets: GetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87928-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87928-120">-ResourceGroupName</span></span>
<span data-ttu-id="87928-121">이 cmdlet가 API Management 서비스를 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87928-121">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroup, GetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87928-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87928-122">CommonParameters</span></span>
<span data-ttu-id="87928-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="87928-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87928-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87928-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87928-125">입력</span><span class="sxs-lookup"><span data-stu-id="87928-125">INPUTS</span></span>

### <span data-ttu-id="87928-126">않아야</span><span class="sxs-lookup"><span data-stu-id="87928-126">None</span></span>
<span data-ttu-id="87928-127">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="87928-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="87928-128">출력</span><span class="sxs-lookup"><span data-stu-id="87928-128">OUTPUTS</span></span>

### <span data-ttu-id="87928-129">ApiManagement의 ' 1 [Microsoft Azure. PsApiManagement] 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="87928-129">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement]</span></span>

## <span data-ttu-id="87928-130">상속자</span><span class="sxs-lookup"><span data-stu-id="87928-130">NOTES</span></span>

## <span data-ttu-id="87928-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="87928-131">RELATED LINKS</span></span>

[<span data-ttu-id="87928-132">백업-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="87928-132">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="87928-133">새로운 AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="87928-133">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="87928-134">제거-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="87928-134">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="87928-135">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="87928-135">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


