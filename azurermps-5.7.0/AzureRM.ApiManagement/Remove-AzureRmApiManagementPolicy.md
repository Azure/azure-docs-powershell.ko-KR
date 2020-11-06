---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 67cff03f8531ff71170fe565d5da411ca5b4f127
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525403"
---
# <span data-ttu-id="1eda3-101">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1eda3-101">Remove-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="1eda3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1eda3-102">SYNOPSIS</span></span>
<span data-ttu-id="1eda3-103">지정 된 범위에서 API 관리 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1eda3-103">Removes the API Management policy from a specified scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1eda3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1eda3-104">SYNTAX</span></span>

### <span data-ttu-id="1eda3-105">RemoveTenantLevel (기본값)</span><span class="sxs-lookup"><span data-stu-id="1eda3-105">RemoveTenantLevel (Default)</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1eda3-106">Remove제품 수준</span><span class="sxs-lookup"><span data-stu-id="1eda3-106">RemoveProductLevel</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1eda3-107">RemoveApiLevel</span><span class="sxs-lookup"><span data-stu-id="1eda3-107">RemoveApiLevel</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1eda3-108">RemoveOperationLevel</span><span class="sxs-lookup"><span data-stu-id="1eda3-108">RemoveOperationLevel</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1eda3-109">설명은</span><span class="sxs-lookup"><span data-stu-id="1eda3-109">DESCRIPTION</span></span>
<span data-ttu-id="1eda3-110">**AzureRmApiManagementPolicy** cmdlet은 지정 된 범위에서 API 관리 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1eda3-110">The **Remove-AzureRmApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="1eda3-111">예제의</span><span class="sxs-lookup"><span data-stu-id="1eda3-111">EXAMPLES</span></span>

### <span data-ttu-id="1eda3-112">예제 1: 테 넌 트 수준 정책 제거</span><span class="sxs-lookup"><span data-stu-id="1eda3-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext
```

<span data-ttu-id="1eda3-113">이 명령은 API Management에서 테 넌 트 수준 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1eda3-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="1eda3-114">예제 2: 제품 범위 정책 제거</span><span class="sxs-lookup"><span data-stu-id="1eda3-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="1eda3-115">이 명령은 API Management에서 제품 범위 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1eda3-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="1eda3-116">예제 3: API 범위 정책 제거</span><span class="sxs-lookup"><span data-stu-id="1eda3-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="1eda3-117">이 명령은 api 관리에서 API 범위 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1eda3-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="1eda3-118">예제 4: 작업 범위 정책 제거</span><span class="sxs-lookup"><span data-stu-id="1eda3-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="1eda3-119">이 명령은 API Management에서 작업 범위 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1eda3-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="1eda3-120">변수</span><span class="sxs-lookup"><span data-stu-id="1eda3-120">PARAMETERS</span></span>

### <span data-ttu-id="1eda3-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="1eda3-121">-ApiId</span></span>
<span data-ttu-id="1eda3-122">기존 API의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1eda3-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="1eda3-123">이 매개 변수를 지정 하면 cmdlet이 API 범위 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1eda3-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: RemoveApiLevel, RemoveOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1eda3-124">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="1eda3-124">-Context</span></span>
<span data-ttu-id="1eda3-125">**PsApiManagementContext** 개체의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1eda3-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1eda3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eda3-126">-DefaultProfile</span></span>
<span data-ttu-id="1eda3-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1eda3-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="1eda3-128">-OperationId</span><span class="sxs-lookup"><span data-stu-id="1eda3-128">-OperationId</span></span>
<span data-ttu-id="1eda3-129">기존 작업의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1eda3-129">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="1eda3-130">*Apiid* 매개 변수를 사용 하 여이 매개 변수를 지정 하면이 cmdlet은 작업 범위 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1eda3-130">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: RemoveOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1eda3-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1eda3-131">-PassThru</span></span>
<span data-ttu-id="1eda3-132">이 cmdlet이 $True 값을 반환 하거나, 성공할 경우, $False의 값이 반환 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1eda3-132">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1eda3-133">-ProductId</span><span class="sxs-lookup"><span data-stu-id="1eda3-133">-ProductId</span></span>
<span data-ttu-id="1eda3-134">기존 제품의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1eda3-134">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="1eda3-135">이 매개 변수를 지정 하면 cmdlet이 제품 범위 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1eda3-135">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: RemoveProductLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1eda3-136">-확인</span><span class="sxs-lookup"><span data-stu-id="1eda3-136">-Confirm</span></span>
<span data-ttu-id="1eda3-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1eda3-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eda3-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1eda3-138">-WhatIf</span></span>
<span data-ttu-id="1eda3-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1eda3-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1eda3-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1eda3-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eda3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eda3-141">CommonParameters</span></span>
<span data-ttu-id="1eda3-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1eda3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eda3-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1eda3-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eda3-144">입력</span><span class="sxs-lookup"><span data-stu-id="1eda3-144">INPUTS</span></span>

### <span data-ttu-id="1eda3-145">않아야</span><span class="sxs-lookup"><span data-stu-id="1eda3-145">None</span></span>
<span data-ttu-id="1eda3-146">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1eda3-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1eda3-147">출력</span><span class="sxs-lookup"><span data-stu-id="1eda3-147">OUTPUTS</span></span>

### <span data-ttu-id="1eda3-148">나타내는</span><span class="sxs-lookup"><span data-stu-id="1eda3-148">Boolean</span></span>

## <span data-ttu-id="1eda3-149">상속자</span><span class="sxs-lookup"><span data-stu-id="1eda3-149">NOTES</span></span>

## <span data-ttu-id="1eda3-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1eda3-150">RELATED LINKS</span></span>

[<span data-ttu-id="1eda3-151">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1eda3-151">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="1eda3-152">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1eda3-152">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


