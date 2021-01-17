---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproductfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
ms.openlocfilehash: a2afd2d5296912606363eddab49e0e3d6b371538
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351249"
---
# <span data-ttu-id="49053-101">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="49053-101">Remove-AzApiManagementProductFromGroup</span></span>

## <span data-ttu-id="49053-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49053-102">SYNOPSIS</span></span>
<span data-ttu-id="49053-103">그룹에서 제품을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="49053-103">Removes a product from a group.</span></span>

## <span data-ttu-id="49053-104">구문</span><span class="sxs-lookup"><span data-stu-id="49053-104">SYNTAX</span></span>

```
Remove-AzApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49053-105">설명</span><span class="sxs-lookup"><span data-stu-id="49053-105">DESCRIPTION</span></span>
<span data-ttu-id="49053-106">**Remove-AzApiManagementProductFromGroup** cmdlet은 기존 그룹에서 제품을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="49053-106">The **Remove-AzApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="49053-107">즉, 이 cmdlet은 제품에서 그룹 할당을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="49053-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="49053-108">예제</span><span class="sxs-lookup"><span data-stu-id="49053-108">EXAMPLES</span></span>

### <span data-ttu-id="49053-109">예제 1: 그룹에서 제품 제거</span><span class="sxs-lookup"><span data-stu-id="49053-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="49053-110">이 명령은 기존 그룹에서 제품을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="49053-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="49053-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49053-111">PARAMETERS</span></span>

### <span data-ttu-id="49053-112">-Context</span><span class="sxs-lookup"><span data-stu-id="49053-112">-Context</span></span>
<span data-ttu-id="49053-113">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="49053-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="49053-114">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="49053-114">This parameter is required.</span></span>

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

### <span data-ttu-id="49053-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49053-115">-DefaultProfile</span></span>
<span data-ttu-id="49053-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="49053-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49053-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="49053-117">-GroupId</span></span>
<span data-ttu-id="49053-118">그룹 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="49053-118">Specifies the group ID.</span></span>
<span data-ttu-id="49053-119">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="49053-119">This parameter is required.</span></span>

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

### <span data-ttu-id="49053-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49053-120">-PassThru</span></span>
<span data-ttu-id="49053-121">이 cmdlet이 성공하는 경우 $True, 그렇지 않은 경우 $False 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="49053-121">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="49053-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="49053-122">-ProductId</span></span>
<span data-ttu-id="49053-123">제품 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="49053-123">Specifies the product ID.</span></span>
<span data-ttu-id="49053-124">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="49053-124">This parameter is required.</span></span>

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

### <span data-ttu-id="49053-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49053-125">CommonParameters</span></span>
<span data-ttu-id="49053-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="49053-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49053-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="49053-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49053-128">입력</span><span class="sxs-lookup"><span data-stu-id="49053-128">INPUTS</span></span>

### <span data-ttu-id="49053-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="49053-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="49053-130">System.String</span><span class="sxs-lookup"><span data-stu-id="49053-130">System.String</span></span>

### <span data-ttu-id="49053-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="49053-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="49053-132">출력</span><span class="sxs-lookup"><span data-stu-id="49053-132">OUTPUTS</span></span>

### <span data-ttu-id="49053-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="49053-133">System.Boolean</span></span>

## <span data-ttu-id="49053-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="49053-134">NOTES</span></span>

## <span data-ttu-id="49053-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49053-135">RELATED LINKS</span></span>

[<span data-ttu-id="49053-136">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="49053-136">Add-AzApiManagementProductToGroup</span></span>](./Add-AzApiManagementProductToGroup.md)


