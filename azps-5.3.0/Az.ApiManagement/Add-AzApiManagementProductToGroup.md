---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
ms.openlocfilehash: a92387392c540c75cfa96ecaf4c4acf026ade9f5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494497"
---
# <span data-ttu-id="68369-101">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="68369-101">Add-AzApiManagementProductToGroup</span></span>

## <span data-ttu-id="68369-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68369-102">SYNOPSIS</span></span>
<span data-ttu-id="68369-103">그룹에 제품을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="68369-103">Adds a product to a group.</span></span>

## <span data-ttu-id="68369-104">구문</span><span class="sxs-lookup"><span data-stu-id="68369-104">SYNTAX</span></span>

```
Add-AzApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68369-105">설명</span><span class="sxs-lookup"><span data-stu-id="68369-105">DESCRIPTION</span></span>
<span data-ttu-id="68369-106">**Add-AzApiManagementProductToGroup** cmdlet은 기존 그룹에 제품을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="68369-106">The **Add-AzApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="68369-107">즉, 이 cmdlet은 제품에 그룹을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="68369-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="68369-108">예제</span><span class="sxs-lookup"><span data-stu-id="68369-108">EXAMPLES</span></span>

### <span data-ttu-id="68369-109">예제 1: 그룹에 제품 추가</span><span class="sxs-lookup"><span data-stu-id="68369-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="68369-110">이 명령은 기존 그룹에 제품을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="68369-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="68369-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68369-111">PARAMETERS</span></span>

### <span data-ttu-id="68369-112">-Context</span><span class="sxs-lookup"><span data-stu-id="68369-112">-Context</span></span>
<span data-ttu-id="68369-113">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="68369-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="68369-114">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="68369-114">This parameter is required.</span></span>

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

### <span data-ttu-id="68369-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68369-115">-DefaultProfile</span></span>
<span data-ttu-id="68369-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68369-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68369-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="68369-117">-GroupId</span></span>
<span data-ttu-id="68369-118">그룹 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="68369-118">Specifies the group ID.</span></span>
<span data-ttu-id="68369-119">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="68369-119">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68369-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68369-120">-PassThru</span></span>
<span data-ttu-id="68369-121">passthru</span><span class="sxs-lookup"><span data-stu-id="68369-121">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68369-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="68369-122">-ProductId</span></span>
<span data-ttu-id="68369-123">제품 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="68369-123">Specifies the product ID.</span></span>
<span data-ttu-id="68369-124">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="68369-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68369-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68369-125">CommonParameters</span></span>
<span data-ttu-id="68369-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="68369-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68369-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="68369-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68369-128">입력</span><span class="sxs-lookup"><span data-stu-id="68369-128">INPUTS</span></span>

### <span data-ttu-id="68369-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="68369-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="68369-130">System.String</span><span class="sxs-lookup"><span data-stu-id="68369-130">System.String</span></span>

### <span data-ttu-id="68369-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="68369-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="68369-132">출력</span><span class="sxs-lookup"><span data-stu-id="68369-132">OUTPUTS</span></span>

### <span data-ttu-id="68369-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="68369-133">System.Boolean</span></span>

## <span data-ttu-id="68369-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="68369-134">NOTES</span></span>

## <span data-ttu-id="68369-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68369-135">RELATED LINKS</span></span>

[<span data-ttu-id="68369-136">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="68369-136">Remove-AzApiManagementProductFromGroup</span></span>](./Remove-AzApiManagementProductFromGroup.md)


