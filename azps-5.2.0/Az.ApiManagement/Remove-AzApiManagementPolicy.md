---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
ms.openlocfilehash: a51bd7aed5ca8793a921c2cde7729c5280df44b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351254"
---
# <span data-ttu-id="7200d-101">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7200d-101">Remove-AzApiManagementPolicy</span></span>

## <span data-ttu-id="7200d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7200d-102">SYNOPSIS</span></span>
<span data-ttu-id="7200d-103">지정된 범위에서 API Management 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7200d-103">Removes the API Management policy from a specified scope.</span></span>

## <span data-ttu-id="7200d-104">구문</span><span class="sxs-lookup"><span data-stu-id="7200d-104">SYNTAX</span></span>

### <span data-ttu-id="7200d-105">RemoveTenantLevel(기본값)</span><span class="sxs-lookup"><span data-stu-id="7200d-105">RemoveTenantLevel (Default)</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7200d-106">RemoveProductLevel</span><span class="sxs-lookup"><span data-stu-id="7200d-106">RemoveProductLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7200d-107">RemoveApiLevel</span><span class="sxs-lookup"><span data-stu-id="7200d-107">RemoveApiLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7200d-108">RemoveOperationLevel</span><span class="sxs-lookup"><span data-stu-id="7200d-108">RemoveOperationLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7200d-109">설명</span><span class="sxs-lookup"><span data-stu-id="7200d-109">DESCRIPTION</span></span>
<span data-ttu-id="7200d-110">**Remove-AzApiManagementPolicy** cmdlet은 지정된 범위에서 API Management 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7200d-110">The **Remove-AzApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="7200d-111">예제</span><span class="sxs-lookup"><span data-stu-id="7200d-111">EXAMPLES</span></span>

### <span data-ttu-id="7200d-112">예제 1: 테넌트 수준 정책 제거</span><span class="sxs-lookup"><span data-stu-id="7200d-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext
```

<span data-ttu-id="7200d-113">이 명령은 API Management에서 테넌트 수준 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7200d-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="7200d-114">예제 2: 제품 범위 정책 제거</span><span class="sxs-lookup"><span data-stu-id="7200d-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="7200d-115">이 명령은 API Management에서 제품 범위 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7200d-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="7200d-116">예제 3: API 범위 정책 제거</span><span class="sxs-lookup"><span data-stu-id="7200d-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="7200d-117">이 명령은 API Management에서 API 범위 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7200d-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="7200d-118">예제 4: 작업 범위 정책 제거</span><span class="sxs-lookup"><span data-stu-id="7200d-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="7200d-119">이 명령은 API Management에서 작업 범위 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7200d-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="7200d-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7200d-120">PARAMETERS</span></span>

### <span data-ttu-id="7200d-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="7200d-121">-ApiId</span></span>
<span data-ttu-id="7200d-122">기존 API의 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7200d-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="7200d-123">이 매개 변수를 지정하면 cmdlet에서 API 범위 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7200d-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveApiLevel, RemoveOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7200d-124">-Context</span><span class="sxs-lookup"><span data-stu-id="7200d-124">-Context</span></span>
<span data-ttu-id="7200d-125">**PsApiManagementContext** 개체의 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7200d-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7200d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7200d-126">-DefaultProfile</span></span>
<span data-ttu-id="7200d-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7200d-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7200d-128">-OperationId</span><span class="sxs-lookup"><span data-stu-id="7200d-128">-OperationId</span></span>
<span data-ttu-id="7200d-129">기존 작업의 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7200d-129">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="7200d-130">*ApiId* 매개 변수를 사용하여 이 매개 변수를 지정하면 이 cmdlet은 작업 범위 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7200d-130">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7200d-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7200d-131">-PassThru</span></span>
<span data-ttu-id="7200d-132">이 cmdlet이 성공하는 경우 $True 값이 반환되거나, 그렇지 않으면 $False 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7200d-132">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="7200d-133">-ProductId</span><span class="sxs-lookup"><span data-stu-id="7200d-133">-ProductId</span></span>
<span data-ttu-id="7200d-134">기존 제품의 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7200d-134">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="7200d-135">이 매개 변수를 지정하면 cmdlet에서 제품 범위 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7200d-135">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7200d-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7200d-136">-Confirm</span></span>
<span data-ttu-id="7200d-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7200d-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7200d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7200d-138">-WhatIf</span></span>
<span data-ttu-id="7200d-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7200d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7200d-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7200d-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7200d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7200d-141">CommonParameters</span></span>
<span data-ttu-id="7200d-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7200d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7200d-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7200d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7200d-144">입력</span><span class="sxs-lookup"><span data-stu-id="7200d-144">INPUTS</span></span>

### <span data-ttu-id="7200d-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7200d-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7200d-146">System.String</span><span class="sxs-lookup"><span data-stu-id="7200d-146">System.String</span></span>

### <span data-ttu-id="7200d-147">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7200d-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7200d-148">출력</span><span class="sxs-lookup"><span data-stu-id="7200d-148">OUTPUTS</span></span>

### <span data-ttu-id="7200d-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7200d-149">System.Boolean</span></span>

## <span data-ttu-id="7200d-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7200d-150">NOTES</span></span>

## <span data-ttu-id="7200d-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7200d-151">RELATED LINKS</span></span>

[<span data-ttu-id="7200d-152">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7200d-152">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="7200d-153">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7200d-153">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


