---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 31b38d07aea51ad1e6bd097cc0c9f7f342e1bfb2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529967"
---
# <span data-ttu-id="31b8e-101">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="31b8e-101">Get-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="31b8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31b8e-102">SYNOPSIS</span></span>
<span data-ttu-id="31b8e-103">지정 된 범위 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="31b8e-103">Gets the specified scope policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31b8e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="31b8e-104">SYNTAX</span></span>

### <span data-ttu-id="31b8e-105">GetTenantLevel (기본값)</span><span class="sxs-lookup"><span data-stu-id="31b8e-105">GetTenantLevel (Default)</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31b8e-106">Get제품 수준</span><span class="sxs-lookup"><span data-stu-id="31b8e-106">GetProductLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="31b8e-107">GetApiLevel</span><span class="sxs-lookup"><span data-stu-id="31b8e-107">GetApiLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31b8e-108">GetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="31b8e-108">GetOperationLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> -OperationId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="31b8e-109">설명은</span><span class="sxs-lookup"><span data-stu-id="31b8e-109">DESCRIPTION</span></span>
<span data-ttu-id="31b8e-110">**AzureRmApiManagementPolicy** cmdlet은 지정 된 범위 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="31b8e-110">The **Get-AzureRmApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="31b8e-111">예제의</span><span class="sxs-lookup"><span data-stu-id="31b8e-111">EXAMPLES</span></span>

### <span data-ttu-id="31b8e-112">예제 1: 테 넌 트 수준 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="31b8e-112">Example 1: Get the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="31b8e-113">이 명령은 테 넌 트 수준 정책을 가져와 tenantpolicy.xml 라는 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b8e-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="31b8e-114">예제 2: 제품 범위 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="31b8e-114">Example 2: Get the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="31b8e-115">이 명령은 제품 범위 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="31b8e-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="31b8e-116">예제 3: API 범위 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="31b8e-116">Example 3: Get the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="31b8e-117">이 명령은 API 범위 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="31b8e-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="31b8e-118">예제 4: 작업 범위 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="31b8e-118">Example 4: Get the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="31b8e-119">이 명령은 작업 범위 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="31b8e-119">This command gets the operation-scope policy.</span></span>

## <span data-ttu-id="31b8e-120">변수</span><span class="sxs-lookup"><span data-stu-id="31b8e-120">PARAMETERS</span></span>

### <span data-ttu-id="31b8e-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="31b8e-121">-ApiId</span></span>
<span data-ttu-id="31b8e-122">기존 API의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b8e-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="31b8e-123">이 매개 변수를 지정 하면 cmdlet이 API 범위 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b8e-123">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31b8e-124">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="31b8e-124">-Context</span></span>
<span data-ttu-id="31b8e-125">**PsApiManagementContext** 의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b8e-125">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="31b8e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b8e-126">-DefaultProfile</span></span>
<span data-ttu-id="31b8e-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="31b8e-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="31b8e-128">-Force</span><span class="sxs-lookup"><span data-stu-id="31b8e-128">-Force</span></span>
<span data-ttu-id="31b8e-129">ps_force</span><span class="sxs-lookup"><span data-stu-id="31b8e-129">ps_force</span></span>

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

### <span data-ttu-id="31b8e-130">-형식</span><span class="sxs-lookup"><span data-stu-id="31b8e-130">-Format</span></span>
<span data-ttu-id="31b8e-131">API 관리 정책의 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b8e-131">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="31b8e-132">이 매개 변수의 기본값은 "application/vnd. policy + xml"입니다.</span><span class="sxs-lookup"><span data-stu-id="31b8e-132">The default value for this parameter is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="31b8e-133">-OperationId</span><span class="sxs-lookup"><span data-stu-id="31b8e-133">-OperationId</span></span>
<span data-ttu-id="31b8e-134">기존 API 작업의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b8e-134">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="31b8e-135">*Apiid* 에이 매개 변수를 지정 하는 경우 cmdlet은 작업 범위 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b8e-135">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: GetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31b8e-136">-ProductId</span><span class="sxs-lookup"><span data-stu-id="31b8e-136">-ProductId</span></span>
<span data-ttu-id="31b8e-137">기존 제품의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b8e-137">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="31b8e-138">이 매개 변수를 지정 하는 경우 cmdlet은 제품 범위 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b8e-138">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: GetProductLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31b8e-139">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="31b8e-139">-SaveAs</span></span>
<span data-ttu-id="31b8e-140">결과를 저장할 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b8e-140">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="31b8e-141">이 매개 변수를 지정 하지 않으면 결과는 sting로 파이프라인 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31b8e-141">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="31b8e-142">-확인</span><span class="sxs-lookup"><span data-stu-id="31b8e-142">-Confirm</span></span>
<span data-ttu-id="31b8e-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b8e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31b8e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31b8e-144">-WhatIf</span></span>
<span data-ttu-id="31b8e-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="31b8e-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31b8e-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31b8e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31b8e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b8e-147">CommonParameters</span></span>
<span data-ttu-id="31b8e-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b8e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b8e-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31b8e-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b8e-150">입력</span><span class="sxs-lookup"><span data-stu-id="31b8e-150">INPUTS</span></span>

### <span data-ttu-id="31b8e-151">않아야</span><span class="sxs-lookup"><span data-stu-id="31b8e-151">None</span></span>
<span data-ttu-id="31b8e-152">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31b8e-152">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="31b8e-153">출력</span><span class="sxs-lookup"><span data-stu-id="31b8e-153">OUTPUTS</span></span>

### <span data-ttu-id="31b8e-154">이름</span><span class="sxs-lookup"><span data-stu-id="31b8e-154">String</span></span>

## <span data-ttu-id="31b8e-155">상속자</span><span class="sxs-lookup"><span data-stu-id="31b8e-155">NOTES</span></span>

## <span data-ttu-id="31b8e-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31b8e-156">RELATED LINKS</span></span>

[<span data-ttu-id="31b8e-157">제거-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="31b8e-157">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="31b8e-158">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="31b8e-158">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


