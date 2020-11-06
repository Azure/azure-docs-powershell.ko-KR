---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
ms.openlocfilehash: 0c28742eb3c774adb8c7b6a8d920e91377bea35f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531880"
---
# <span data-ttu-id="2c9f6-101">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2c9f6-101">Get-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="2c9f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c9f6-102">SYNOPSIS</span></span>
<span data-ttu-id="2c9f6-103">모든 또는 특정 API 관리 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2c9f6-103">Gets all or specific API management groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c9f6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2c9f6-104">SYNTAX</span></span>

### <span data-ttu-id="2c9f6-105">모든 그룹 가져오기 (기본값)</span><span class="sxs-lookup"><span data-stu-id="2c9f6-105">Get all groups (Default)</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c9f6-106">그룹 ID로 가져오기</span><span class="sxs-lookup"><span data-stu-id="2c9f6-106">Get by group ID</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c9f6-107">사용자별로 그룹 찾기</span><span class="sxs-lookup"><span data-stu-id="2c9f6-107">Find groups by user</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c9f6-108">제품별로 그룹 찾기</span><span class="sxs-lookup"><span data-stu-id="2c9f6-108">Find groups by product</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c9f6-109">설명은</span><span class="sxs-lookup"><span data-stu-id="2c9f6-109">DESCRIPTION</span></span>
<span data-ttu-id="2c9f6-110">**AzureRmApiManagementGroup** cmdlet은 모든 또는 특정 API 관리 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2c9f6-110">The **Get-AzureRmApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="2c9f6-111">예제의</span><span class="sxs-lookup"><span data-stu-id="2c9f6-111">EXAMPLES</span></span>

### <span data-ttu-id="2c9f6-112">예제 1: 모든 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="2c9f6-112">Example 1: Get all groups</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext
```

<span data-ttu-id="2c9f6-113">이 명령은 모든 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2c9f6-113">This command gets all groups.</span></span>

### <span data-ttu-id="2c9f6-114">예제 2: ID를 기준으로 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="2c9f6-114">Example 2: Get a group by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext -GroupId "0123456789"
```

<span data-ttu-id="2c9f6-115">이 명령은 0123456789 이라는 그룹 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2c9f6-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="2c9f6-116">예제 3: 이름으로 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="2c9f6-116">Example 3: Get a group by name</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext -Name "Group0002"
```

<span data-ttu-id="2c9f6-117">이 명령은 Group0002 이라는 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2c9f6-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="2c9f6-118">예제 4: 모든 사용자 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="2c9f6-118">Example 4: Get all user groups</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext -UserId "0123456789"
```

<span data-ttu-id="2c9f6-119">이 명령은 0123456789 이라는 이름의 사용자 ID를 사용 하 여 모든 사용자 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2c9f6-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="2c9f6-120">변수</span><span class="sxs-lookup"><span data-stu-id="2c9f6-120">PARAMETERS</span></span>

### <span data-ttu-id="2c9f6-121">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="2c9f6-121">-Context</span></span>
<span data-ttu-id="2c9f6-122">PsApiManagementContext의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c9f6-122">Specifies an instance of PsApiManagementContext.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c9f6-123">-GroupId</span><span class="sxs-lookup"><span data-stu-id="2c9f6-123">-GroupId</span></span>
<span data-ttu-id="2c9f6-124">그룹 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c9f6-124">Specifies the group ID.</span></span>
<span data-ttu-id="2c9f6-125">지정 된 경우 cmdlet은 식별자를 기준으로 그룹을 찾으려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c9f6-125">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by group ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c9f6-126">-이름</span><span class="sxs-lookup"><span data-stu-id="2c9f6-126">-Name</span></span>
<span data-ttu-id="2c9f6-127">관리 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c9f6-127">Specifies the name of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c9f6-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="2c9f6-128">-ProductId</span></span>
<span data-ttu-id="2c9f6-129">기존 제품의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="2c9f6-129">Identifier of existing product.</span></span>
<span data-ttu-id="2c9f6-130">지정 된 경우 제품에 할당 된 모든 그룹이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2c9f6-130">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="2c9f6-131">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="2c9f6-131">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find groups by product
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c9f6-132">-UserId</span><span class="sxs-lookup"><span data-stu-id="2c9f6-132">-UserId</span></span>
<span data-ttu-id="2c9f6-133">기존 제품의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c9f6-133">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="2c9f6-134">지정 된 경우 cmdlet이 할당 된 제품이 있는 모든 그룹을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c9f6-134">If specified the cmdlet will return all groups the product assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: Find groups by user
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c9f6-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c9f6-135">-DefaultProfile</span></span>
<span data-ttu-id="2c9f6-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2c9f6-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c9f6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c9f6-137">CommonParameters</span></span>
<span data-ttu-id="2c9f6-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c9f6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c9f6-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c9f6-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c9f6-140">입력</span><span class="sxs-lookup"><span data-stu-id="2c9f6-140">INPUTS</span></span>

## <span data-ttu-id="2c9f6-141">출력</span><span class="sxs-lookup"><span data-stu-id="2c9f6-141">OUTPUTS</span></span>

### <span data-ttu-id="2c9f6-142">IList를<ApiManagement> ServiceManagement. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2c9f6-142">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup></span></span>

## <span data-ttu-id="2c9f6-143">상속자</span><span class="sxs-lookup"><span data-stu-id="2c9f6-143">NOTES</span></span>

## <span data-ttu-id="2c9f6-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c9f6-144">RELATED LINKS</span></span>

[<span data-ttu-id="2c9f6-145">새로운 AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2c9f6-145">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="2c9f6-146">제거-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2c9f6-146">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="2c9f6-147">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2c9f6-147">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


