---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
ms.openlocfilehash: c7f88f204bbb6d4999e6ddb1f0f3e2942500daf7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494453"
---
# <span data-ttu-id="237c2-101">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="237c2-101">Get-AzApiManagementGroup</span></span>

## <span data-ttu-id="237c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="237c2-102">SYNOPSIS</span></span>
<span data-ttu-id="237c2-103">전체 또는 특정 API 관리 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="237c2-103">Gets all or specific API management groups.</span></span>

## <span data-ttu-id="237c2-104">구문</span><span class="sxs-lookup"><span data-stu-id="237c2-104">SYNTAX</span></span>

### <span data-ttu-id="237c2-105">GetAllGroups(기본값)</span><span class="sxs-lookup"><span data-stu-id="237c2-105">GetAllGroups (Default)</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="237c2-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="237c2-106">GetByGroupId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="237c2-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="237c2-107">GetByUserId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="237c2-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="237c2-108">GetByProductId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="237c2-109">설명</span><span class="sxs-lookup"><span data-stu-id="237c2-109">DESCRIPTION</span></span>
<span data-ttu-id="237c2-110">**Get-AzApiManagementGroup** cmdlet은 전체 또는 특정 API 관리 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="237c2-110">The **Get-AzApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="237c2-111">예제</span><span class="sxs-lookup"><span data-stu-id="237c2-111">EXAMPLES</span></span>

### <span data-ttu-id="237c2-112">예제 1: 모든 그룹 얻기</span><span class="sxs-lookup"><span data-stu-id="237c2-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext
```

<span data-ttu-id="237c2-113">이 명령은 모든 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="237c2-113">This command gets all groups.</span></span>

### <span data-ttu-id="237c2-114">예제 2: ID로 그룹 얻기</span><span class="sxs-lookup"><span data-stu-id="237c2-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="237c2-115">이 명령은 0123456789라는 그룹 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="237c2-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="237c2-116">예제 3: 이름으로 그룹 얻기</span><span class="sxs-lookup"><span data-stu-id="237c2-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="237c2-117">이 명령은 Group0002라는 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="237c2-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="237c2-118">예제 4: 모든 사용자 그룹 얻기</span><span class="sxs-lookup"><span data-stu-id="237c2-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="237c2-119">이 명령은 0123456789라는 사용자 ID를 사용하여 모든 사용자 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="237c2-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="237c2-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="237c2-120">PARAMETERS</span></span>

### <span data-ttu-id="237c2-121">-Context</span><span class="sxs-lookup"><span data-stu-id="237c2-121">-Context</span></span>
<span data-ttu-id="237c2-122">PsApiManagementContext의 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="237c2-122">Specifies an instance of PsApiManagementContext.</span></span>

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

### <span data-ttu-id="237c2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="237c2-123">-DefaultProfile</span></span>
<span data-ttu-id="237c2-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="237c2-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="237c2-125">-GroupId</span><span class="sxs-lookup"><span data-stu-id="237c2-125">-GroupId</span></span>
<span data-ttu-id="237c2-126">그룹 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="237c2-126">Specifies the group ID.</span></span>
<span data-ttu-id="237c2-127">지정된 경우 cmdlet은 식별자에 의해 그룹을 찾으하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="237c2-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

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

### <span data-ttu-id="237c2-128">-Name</span><span class="sxs-lookup"><span data-stu-id="237c2-128">-Name</span></span>
<span data-ttu-id="237c2-129">관리 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="237c2-129">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="237c2-130">-ProductId</span><span class="sxs-lookup"><span data-stu-id="237c2-130">-ProductId</span></span>
<span data-ttu-id="237c2-131">기존 제품의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="237c2-131">Identifier of existing product.</span></span>
<span data-ttu-id="237c2-132">지정된 경우 할당된 모든 그룹이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="237c2-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="237c2-133">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="237c2-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="237c2-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="237c2-134">-UserId</span></span>
<span data-ttu-id="237c2-135">기존 제품의 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="237c2-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="237c2-136">지정된 경우 cmdlet은 할당된 모든 그룹을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="237c2-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

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

### <span data-ttu-id="237c2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="237c2-137">CommonParameters</span></span>
<span data-ttu-id="237c2-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="237c2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="237c2-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="237c2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="237c2-140">입력</span><span class="sxs-lookup"><span data-stu-id="237c2-140">INPUTS</span></span>

### <span data-ttu-id="237c2-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="237c2-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="237c2-142">System.String</span><span class="sxs-lookup"><span data-stu-id="237c2-142">System.String</span></span>

## <span data-ttu-id="237c2-143">출력</span><span class="sxs-lookup"><span data-stu-id="237c2-143">OUTPUTS</span></span>

### <span data-ttu-id="237c2-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="237c2-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="237c2-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="237c2-145">NOTES</span></span>

## <span data-ttu-id="237c2-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="237c2-146">RELATED LINKS</span></span>

[<span data-ttu-id="237c2-147">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="237c2-147">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="237c2-148">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="237c2-148">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="237c2-149">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="237c2-149">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


