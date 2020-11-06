---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 16eed643397245fa54b2876430042335762ea048
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531292"
---
# <span data-ttu-id="1e699-101">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1e699-101">Get-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="1e699-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e699-102">SYNOPSIS</span></span>
<span data-ttu-id="1e699-103">지정 된 범위 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1e699-103">Gets the specified scope policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e699-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1e699-104">SYNTAX</span></span>

### <span data-ttu-id="1e699-105">테 넌 트 수준 (기본값)</span><span class="sxs-lookup"><span data-stu-id="1e699-105">Tenant level (Default)</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e699-106">제품 수준</span><span class="sxs-lookup"><span data-stu-id="1e699-106">Product level</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e699-107">API 수준</span><span class="sxs-lookup"><span data-stu-id="1e699-107">API level</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e699-108">작업 수준</span><span class="sxs-lookup"><span data-stu-id="1e699-108">Operation level</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> -OperationId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1e699-109">설명은</span><span class="sxs-lookup"><span data-stu-id="1e699-109">DESCRIPTION</span></span>
<span data-ttu-id="1e699-110">**AzureRmApiManagementPolicy** cmdlet은 지정 된 범위 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1e699-110">The **Get-AzureRmApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="1e699-111">예제의</span><span class="sxs-lookup"><span data-stu-id="1e699-111">EXAMPLES</span></span>

### <span data-ttu-id="1e699-112">예제 1: 테 넌 트 수준 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="1e699-112">Example 1: Get the tenant level policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="1e699-113">이 명령은 테 넌 트 수준 정책을 가져와 tenantpolicy.xml 라는 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e699-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="1e699-114">예제 2: 제품 범위 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="1e699-114">Example 2: Get the product-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789"
```

<span data-ttu-id="1e699-115">이 명령은 제품 범위 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1e699-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="1e699-116">예제 3: API 범위 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="1e699-116">Example 3: Get the API-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210"
```

<span data-ttu-id="1e699-117">이 명령은 API 범위 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1e699-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="1e699-118">예제 4: 작업 범위 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="1e699-118">Example 4: Get the operation-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="1e699-119">이 명령은 작업 범위 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1e699-119">This command gets the operation-scope policy.</span></span>

## <span data-ttu-id="1e699-120">변수</span><span class="sxs-lookup"><span data-stu-id="1e699-120">PARAMETERS</span></span>

### <span data-ttu-id="1e699-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="1e699-121">-ApiId</span></span>
<span data-ttu-id="1e699-122">기존 API의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e699-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="1e699-123">이 매개 변수를 지정 하면 cmdlet이 API 범위 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e699-123">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: API level, Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e699-124">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="1e699-124">-Context</span></span>
<span data-ttu-id="1e699-125">**PsApiManagementContext** 의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e699-125">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="1e699-126">-Force</span><span class="sxs-lookup"><span data-stu-id="1e699-126">-Force</span></span>
<span data-ttu-id="1e699-127">ps_force</span><span class="sxs-lookup"><span data-stu-id="1e699-127">ps_force</span></span>

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

### <span data-ttu-id="1e699-128">-형식</span><span class="sxs-lookup"><span data-stu-id="1e699-128">-Format</span></span>
<span data-ttu-id="1e699-129">API 관리 정책의 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e699-129">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="1e699-130">이 매개 변수의 기본값은 "application/vnd. policy + xml"입니다.</span><span class="sxs-lookup"><span data-stu-id="1e699-130">The default value for this parameter is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="1e699-131">-OperationId</span><span class="sxs-lookup"><span data-stu-id="1e699-131">-OperationId</span></span>
<span data-ttu-id="1e699-132">기존 API 작업의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e699-132">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="1e699-133">*Apiid* 에이 매개 변수를 지정 하는 경우 cmdlet은 작업 범위 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e699-133">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e699-134">-ProductId</span><span class="sxs-lookup"><span data-stu-id="1e699-134">-ProductId</span></span>
<span data-ttu-id="1e699-135">기존 제품의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e699-135">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="1e699-136">이 매개 변수를 지정 하는 경우 cmdlet은 제품 범위 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e699-136">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: Product level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e699-137">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="1e699-137">-SaveAs</span></span>
<span data-ttu-id="1e699-138">결과를 저장할 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e699-138">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="1e699-139">이 매개 변수를 지정 하지 않으면 결과는 sting로 파이프라인 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e699-139">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="1e699-140">-확인</span><span class="sxs-lookup"><span data-stu-id="1e699-140">-Confirm</span></span>
<span data-ttu-id="1e699-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e699-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e699-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e699-142">-WhatIf</span></span>
<span data-ttu-id="1e699-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1e699-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e699-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e699-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e699-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e699-145">-DefaultProfile</span></span>
<span data-ttu-id="1e699-146">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1e699-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e699-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e699-147">CommonParameters</span></span>
<span data-ttu-id="1e699-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e699-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e699-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e699-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e699-150">입력</span><span class="sxs-lookup"><span data-stu-id="1e699-150">INPUTS</span></span>

## <span data-ttu-id="1e699-151">출력</span><span class="sxs-lookup"><span data-stu-id="1e699-151">OUTPUTS</span></span>

### <span data-ttu-id="1e699-152">이름</span><span class="sxs-lookup"><span data-stu-id="1e699-152">String</span></span>

## <span data-ttu-id="1e699-153">상속자</span><span class="sxs-lookup"><span data-stu-id="1e699-153">NOTES</span></span>

## <span data-ttu-id="1e699-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1e699-154">RELATED LINKS</span></span>

[<span data-ttu-id="1e699-155">제거-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1e699-155">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="1e699-156">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1e699-156">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


