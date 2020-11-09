---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
ms.openlocfilehash: c7f88f204bbb6d4999e6ddb1f0f3e2942500daf7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307664"
---
# <span data-ttu-id="a8a03-101">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a8a03-101">Get-AzApiManagementGroup</span></span>

## <span data-ttu-id="a8a03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8a03-102">SYNOPSIS</span></span>
<span data-ttu-id="a8a03-103">모든 또는 특정 API 관리 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a8a03-103">Gets all or specific API management groups.</span></span>

## <span data-ttu-id="a8a03-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a8a03-104">SYNTAX</span></span>

### <span data-ttu-id="a8a03-105">GetAllGroups (기본값)</span><span class="sxs-lookup"><span data-stu-id="a8a03-105">GetAllGroups (Default)</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8a03-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="a8a03-106">GetByGroupId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8a03-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="a8a03-107">GetByUserId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8a03-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="a8a03-108">GetByProductId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8a03-109">설명은</span><span class="sxs-lookup"><span data-stu-id="a8a03-109">DESCRIPTION</span></span>
<span data-ttu-id="a8a03-110">**AzApiManagementGroup** cmdlet은 모든 또는 특정 API 관리 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a8a03-110">The **Get-AzApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="a8a03-111">예제의</span><span class="sxs-lookup"><span data-stu-id="a8a03-111">EXAMPLES</span></span>

### <span data-ttu-id="a8a03-112">예제 1: 모든 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="a8a03-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext
```

<span data-ttu-id="a8a03-113">이 명령은 모든 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a8a03-113">This command gets all groups.</span></span>

### <span data-ttu-id="a8a03-114">예제 2: ID를 기준으로 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="a8a03-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="a8a03-115">이 명령은 0123456789 이라는 그룹 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a8a03-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="a8a03-116">예제 3: 이름으로 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="a8a03-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="a8a03-117">이 명령은 Group0002 이라는 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a8a03-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="a8a03-118">예제 4: 모든 사용자 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="a8a03-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="a8a03-119">이 명령은 0123456789 이라는 이름의 사용자 ID를 사용 하 여 모든 사용자 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a8a03-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="a8a03-120">변수</span><span class="sxs-lookup"><span data-stu-id="a8a03-120">PARAMETERS</span></span>

### <span data-ttu-id="a8a03-121">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="a8a03-121">-Context</span></span>
<span data-ttu-id="a8a03-122">PsApiManagementContext의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8a03-122">Specifies an instance of PsApiManagementContext.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8a03-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8a03-123">-DefaultProfile</span></span>
<span data-ttu-id="a8a03-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a8a03-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8a03-125">-GroupId</span><span class="sxs-lookup"><span data-stu-id="a8a03-125">-GroupId</span></span>
<span data-ttu-id="a8a03-126">그룹 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8a03-126">Specifies the group ID.</span></span>
<span data-ttu-id="a8a03-127">지정 된 경우 cmdlet은 식별자를 기준으로 그룹을 찾으려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8a03-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGroupId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8a03-128">-이름</span><span class="sxs-lookup"><span data-stu-id="a8a03-128">-Name</span></span>
<span data-ttu-id="a8a03-129">관리 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8a03-129">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="a8a03-130">-ProductId</span><span class="sxs-lookup"><span data-stu-id="a8a03-130">-ProductId</span></span>
<span data-ttu-id="a8a03-131">기존 제품의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a8a03-131">Identifier of existing product.</span></span>
<span data-ttu-id="a8a03-132">지정 된 경우 제품에 할당 된 모든 그룹이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8a03-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="a8a03-133">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="a8a03-133">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8a03-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="a8a03-134">-UserId</span></span>
<span data-ttu-id="a8a03-135">기존 제품의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8a03-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="a8a03-136">지정 된 경우 cmdlet이 할당 된 제품이 있는 모든 그룹을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8a03-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8a03-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8a03-137">CommonParameters</span></span>
<span data-ttu-id="a8a03-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8a03-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8a03-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a8a03-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8a03-140">입력</span><span class="sxs-lookup"><span data-stu-id="a8a03-140">INPUTS</span></span>

### <span data-ttu-id="a8a03-141">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a8a03-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a8a03-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a8a03-142">System.String</span></span>

## <span data-ttu-id="a8a03-143">출력</span><span class="sxs-lookup"><span data-stu-id="a8a03-143">OUTPUTS</span></span>

### <span data-ttu-id="a8a03-144">ApiManagement. ServiceManagement. \ PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a8a03-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="a8a03-145">상속자</span><span class="sxs-lookup"><span data-stu-id="a8a03-145">NOTES</span></span>

## <span data-ttu-id="a8a03-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a8a03-146">RELATED LINKS</span></span>

[<span data-ttu-id="a8a03-147">새로운 AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a8a03-147">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="a8a03-148">제거-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a8a03-148">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="a8a03-149">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a8a03-149">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


