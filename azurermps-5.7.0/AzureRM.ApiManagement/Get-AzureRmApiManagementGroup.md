---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
ms.openlocfilehash: b77452bff93a9b66f8ffe54fdff623d391749622
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532864"
---
# <span data-ttu-id="f738b-101">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f738b-101">Get-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="f738b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f738b-102">SYNOPSIS</span></span>
<span data-ttu-id="f738b-103">모든 또는 특정 API 관리 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f738b-103">Gets all or specific API management groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f738b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f738b-104">SYNTAX</span></span>

### <span data-ttu-id="f738b-105">GetAllGroups (기본값)</span><span class="sxs-lookup"><span data-stu-id="f738b-105">GetAllGroups (Default)</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f738b-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="f738b-106">GetByGroupId</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f738b-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="f738b-107">GetByUserId</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f738b-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="f738b-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f738b-109">설명은</span><span class="sxs-lookup"><span data-stu-id="f738b-109">DESCRIPTION</span></span>
<span data-ttu-id="f738b-110">**AzureRmApiManagementGroup** cmdlet은 모든 또는 특정 API 관리 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f738b-110">The **Get-AzureRmApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="f738b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="f738b-111">EXAMPLES</span></span>

### <span data-ttu-id="f738b-112">예제 1: 모든 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="f738b-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext
```

<span data-ttu-id="f738b-113">이 명령은 모든 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f738b-113">This command gets all groups.</span></span>

### <span data-ttu-id="f738b-114">예제 2: ID를 기준으로 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="f738b-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="f738b-115">이 명령은 0123456789 이라는 그룹 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f738b-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="f738b-116">예제 3: 이름으로 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="f738b-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="f738b-117">이 명령은 Group0002 이라는 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f738b-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="f738b-118">예제 4: 모든 사용자 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="f738b-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="f738b-119">이 명령은 0123456789 이라는 이름의 사용자 ID를 사용 하 여 모든 사용자 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f738b-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="f738b-120">변수</span><span class="sxs-lookup"><span data-stu-id="f738b-120">PARAMETERS</span></span>

### <span data-ttu-id="f738b-121">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="f738b-121">-Context</span></span>
<span data-ttu-id="f738b-122">PsApiManagementContext의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f738b-122">Specifies an instance of PsApiManagementContext.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f738b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f738b-123">-DefaultProfile</span></span>
<span data-ttu-id="f738b-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f738b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="f738b-125">-GroupId</span><span class="sxs-lookup"><span data-stu-id="f738b-125">-GroupId</span></span>
<span data-ttu-id="f738b-126">그룹 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f738b-126">Specifies the group ID.</span></span>
<span data-ttu-id="f738b-127">지정 된 경우 cmdlet은 식별자를 기준으로 그룹을 찾으려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="f738b-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetByGroupId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f738b-128">-이름</span><span class="sxs-lookup"><span data-stu-id="f738b-128">-Name</span></span>
<span data-ttu-id="f738b-129">관리 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f738b-129">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="f738b-130">-ProductId</span><span class="sxs-lookup"><span data-stu-id="f738b-130">-ProductId</span></span>
<span data-ttu-id="f738b-131">기존 제품의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="f738b-131">Identifier of existing product.</span></span>
<span data-ttu-id="f738b-132">지정 된 경우 제품에 할당 된 모든 그룹이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f738b-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="f738b-133">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="f738b-133">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByProductId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f738b-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="f738b-134">-UserId</span></span>
<span data-ttu-id="f738b-135">기존 제품의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f738b-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="f738b-136">지정 된 경우 cmdlet이 할당 된 제품이 있는 모든 그룹을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f738b-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

```yaml
Type: String
Parameter Sets: GetByUserId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f738b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f738b-137">CommonParameters</span></span>
<span data-ttu-id="f738b-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f738b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f738b-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f738b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f738b-140">입력</span><span class="sxs-lookup"><span data-stu-id="f738b-140">INPUTS</span></span>

### <span data-ttu-id="f738b-141">않아야</span><span class="sxs-lookup"><span data-stu-id="f738b-141">None</span></span>
<span data-ttu-id="f738b-142">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f738b-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f738b-143">출력</span><span class="sxs-lookup"><span data-stu-id="f738b-143">OUTPUTS</span></span>

### <span data-ttu-id="f738b-144">ApiManagement. ServiceManagement. \ PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f738b-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>
<span data-ttu-id="f738b-145">API Management 서비스에서 구성 된 그룹의 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="f738b-145">The details of the Group configured in API Management service.</span></span>

### <span data-ttu-id="f738b-146">IList를<ApiManagement> ServiceManagement. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f738b-146">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup></span></span>
<span data-ttu-id="f738b-147">API Management 서비스에 구성 된 그룹 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f738b-147">The list of Groups configured in API Management service.</span></span>

## <span data-ttu-id="f738b-148">상속자</span><span class="sxs-lookup"><span data-stu-id="f738b-148">NOTES</span></span>

## <span data-ttu-id="f738b-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f738b-149">RELATED LINKS</span></span>

[<span data-ttu-id="f738b-150">새로운 AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f738b-150">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="f738b-151">제거-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f738b-151">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="f738b-152">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f738b-152">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


