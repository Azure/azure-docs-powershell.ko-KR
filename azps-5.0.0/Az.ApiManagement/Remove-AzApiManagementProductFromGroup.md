---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproductfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
ms.openlocfilehash: a2afd2d5296912606363eddab49e0e3d6b371538
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310982"
---
# <span data-ttu-id="0d690-101">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="0d690-101">Remove-AzApiManagementProductFromGroup</span></span>

## <span data-ttu-id="0d690-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d690-102">SYNOPSIS</span></span>
<span data-ttu-id="0d690-103">그룹에서 제품을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d690-103">Removes a product from a group.</span></span>

## <span data-ttu-id="0d690-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0d690-104">SYNTAX</span></span>

```
Remove-AzApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d690-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0d690-105">DESCRIPTION</span></span>
<span data-ttu-id="0d690-106">**AzApiManagementProductFromGroup** cmdlet은 기존 그룹의 제품을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d690-106">The **Remove-AzApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="0d690-107">즉,이 cmdlet은 제품에서 그룹 과제를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d690-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="0d690-108">예제의</span><span class="sxs-lookup"><span data-stu-id="0d690-108">EXAMPLES</span></span>

### <span data-ttu-id="0d690-109">예제 1: 그룹에서 제품 제거</span><span class="sxs-lookup"><span data-stu-id="0d690-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="0d690-110">이 명령은 기존 그룹에서 제품을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d690-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="0d690-111">변수</span><span class="sxs-lookup"><span data-stu-id="0d690-111">PARAMETERS</span></span>

### <span data-ttu-id="0d690-112">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="0d690-112">-Context</span></span>
<span data-ttu-id="0d690-113">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d690-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="0d690-114">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="0d690-114">This parameter is required.</span></span>

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

### <span data-ttu-id="0d690-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d690-115">-DefaultProfile</span></span>
<span data-ttu-id="0d690-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0d690-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d690-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="0d690-117">-GroupId</span></span>
<span data-ttu-id="0d690-118">그룹 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d690-118">Specifies the group ID.</span></span>
<span data-ttu-id="0d690-119">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="0d690-119">This parameter is required.</span></span>

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

### <span data-ttu-id="0d690-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d690-120">-PassThru</span></span>
<span data-ttu-id="0d690-121">이 cmdlet이 $True 값을 반환 하거나, 성공할 경우, $False 또는, 그렇지 않은 경우이를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0d690-121">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="0d690-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="0d690-122">-ProductId</span></span>
<span data-ttu-id="0d690-123">제품 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d690-123">Specifies the product ID.</span></span>
<span data-ttu-id="0d690-124">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="0d690-124">This parameter is required.</span></span>

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

### <span data-ttu-id="0d690-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d690-125">CommonParameters</span></span>
<span data-ttu-id="0d690-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d690-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d690-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0d690-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d690-128">입력</span><span class="sxs-lookup"><span data-stu-id="0d690-128">INPUTS</span></span>

### <span data-ttu-id="0d690-129">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0d690-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0d690-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0d690-130">System.String</span></span>

### <span data-ttu-id="0d690-131">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0d690-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0d690-132">출력</span><span class="sxs-lookup"><span data-stu-id="0d690-132">OUTPUTS</span></span>

### <span data-ttu-id="0d690-133">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="0d690-133">System.Boolean</span></span>

## <span data-ttu-id="0d690-134">상속자</span><span class="sxs-lookup"><span data-stu-id="0d690-134">NOTES</span></span>

## <span data-ttu-id="0d690-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d690-135">RELATED LINKS</span></span>

[<span data-ttu-id="0d690-136">추가-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="0d690-136">Add-AzApiManagementProductToGroup</span></span>](./Add-AzApiManagementProductToGroup.md)


