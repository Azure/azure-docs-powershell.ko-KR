---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
ms.openlocfilehash: fcf88fcb9b54adec01b8a04b50f557b6a74e7ca8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524751"
---
# <span data-ttu-id="e3f2e-101">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e3f2e-101">Get-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="e3f2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3f2e-102">SYNOPSIS</span></span>
<span data-ttu-id="e3f2e-103">지정 된 범위 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e3f2e-103">Gets the specified scope policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3f2e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e3f2e-104">SYNTAX</span></span>

### <span data-ttu-id="e3f2e-105">GetTenantLevel (기본값)</span><span class="sxs-lookup"><span data-stu-id="e3f2e-105">GetTenantLevel (Default)</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3f2e-106">Get제품 수준</span><span class="sxs-lookup"><span data-stu-id="e3f2e-106">GetProductLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3f2e-107">GetApiLevel</span><span class="sxs-lookup"><span data-stu-id="e3f2e-107">GetApiLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3f2e-108">GetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="e3f2e-108">GetOperationLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] -OperationId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3f2e-109">설명은</span><span class="sxs-lookup"><span data-stu-id="e3f2e-109">DESCRIPTION</span></span>
<span data-ttu-id="e3f2e-110">**AzureRmApiManagementPolicy** cmdlet은 지정 된 범위 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e3f2e-110">The **Get-AzureRmApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="e3f2e-111">예제의</span><span class="sxs-lookup"><span data-stu-id="e3f2e-111">EXAMPLES</span></span>

### <span data-ttu-id="e3f2e-112">예제 1: 테 넌 트 수준 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="e3f2e-112">Example 1: Get the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="e3f2e-113">이 명령은 테 넌 트 수준 정책을 가져와 tenantpolicy.xml 라는 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3f2e-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="e3f2e-114">예제 2: 제품 범위 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="e3f2e-114">Example 2: Get the product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="e3f2e-115">이 명령은 제품 범위 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e3f2e-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="e3f2e-116">예제 3: API 범위 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="e3f2e-116">Example 3: Get the API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="e3f2e-117">이 명령은 API 범위 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e3f2e-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="e3f2e-118">예제 4: 작업 범위 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="e3f2e-118">Example 4: Get the operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="e3f2e-119">이 명령은 작업 범위 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e3f2e-119">This command gets the operation-scope policy.</span></span>

## <span data-ttu-id="e3f2e-120">변수</span><span class="sxs-lookup"><span data-stu-id="e3f2e-120">PARAMETERS</span></span>

### <span data-ttu-id="e3f2e-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e3f2e-121">-ApiId</span></span>
<span data-ttu-id="e3f2e-122">기존 API의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3f2e-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="e3f2e-123">이 매개 변수를 지정 하면 cmdlet이 API 범위 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3f2e-123">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f2e-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="e3f2e-124">-ApiRevision</span></span>
<span data-ttu-id="e3f2e-125">API 개정판의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e3f2e-125">Identifier of API Revision.</span></span> <span data-ttu-id="e3f2e-126">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="e3f2e-126">This parameter is optional.</span></span> <span data-ttu-id="e3f2e-127">지정 하지 않으면 현재 활성 api 개정판에서 정책이 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3f2e-127">If not specified, the policy will be retrieved from the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f2e-128">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="e3f2e-128">-Context</span></span>
<span data-ttu-id="e3f2e-129">**PsApiManagementContext** 의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3f2e-129">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="e3f2e-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3f2e-130">-DefaultProfile</span></span>
<span data-ttu-id="e3f2e-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e3f2e-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3f2e-132">-Force</span><span class="sxs-lookup"><span data-stu-id="e3f2e-132">-Force</span></span>
<span data-ttu-id="e3f2e-133">ps_force</span><span class="sxs-lookup"><span data-stu-id="e3f2e-133">ps_force</span></span>

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

### <span data-ttu-id="e3f2e-134">-형식</span><span class="sxs-lookup"><span data-stu-id="e3f2e-134">-Format</span></span>
<span data-ttu-id="e3f2e-135">API 관리 정책의 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3f2e-135">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="e3f2e-136">이 매개 변수의 기본값은 "application/vnd. policy + xml"입니다.</span><span class="sxs-lookup"><span data-stu-id="e3f2e-136">The default value for this parameter is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="e3f2e-137">-OperationId</span><span class="sxs-lookup"><span data-stu-id="e3f2e-137">-OperationId</span></span>
<span data-ttu-id="e3f2e-138">기존 API 작업의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3f2e-138">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="e3f2e-139">*Apiid* 에이 매개 변수를 지정 하는 경우 cmdlet은 작업 범위 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3f2e-139">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f2e-140">-ProductId</span><span class="sxs-lookup"><span data-stu-id="e3f2e-140">-ProductId</span></span>
<span data-ttu-id="e3f2e-141">기존 제품의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3f2e-141">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="e3f2e-142">이 매개 변수를 지정 하는 경우 cmdlet은 제품 범위 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3f2e-142">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f2e-143">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="e3f2e-143">-SaveAs</span></span>
<span data-ttu-id="e3f2e-144">결과를 저장할 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3f2e-144">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="e3f2e-145">이 매개 변수를 지정 하지 않으면 결과는 sting로 파이프라인 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3f2e-145">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="e3f2e-146">-확인</span><span class="sxs-lookup"><span data-stu-id="e3f2e-146">-Confirm</span></span>
<span data-ttu-id="e3f2e-147">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3f2e-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3f2e-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3f2e-148">-WhatIf</span></span>
<span data-ttu-id="e3f2e-149">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e3f2e-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3f2e-150">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e3f2e-150">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3f2e-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3f2e-151">CommonParameters</span></span>
<span data-ttu-id="e3f2e-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3f2e-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3f2e-153">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3f2e-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3f2e-154">입력</span><span class="sxs-lookup"><span data-stu-id="e3f2e-154">INPUTS</span></span>

### <span data-ttu-id="e3f2e-155">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e3f2e-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e3f2e-156">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e3f2e-156">System.String</span></span>

### <span data-ttu-id="e3f2e-157">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e3f2e-157">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e3f2e-158">출력</span><span class="sxs-lookup"><span data-stu-id="e3f2e-158">OUTPUTS</span></span>

### <span data-ttu-id="e3f2e-159">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e3f2e-159">System.String</span></span>

## <span data-ttu-id="e3f2e-160">상속자</span><span class="sxs-lookup"><span data-stu-id="e3f2e-160">NOTES</span></span>

## <span data-ttu-id="e3f2e-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3f2e-161">RELATED LINKS</span></span>

[<span data-ttu-id="e3f2e-162">제거-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e3f2e-162">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="e3f2e-163">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e3f2e-163">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


