---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
ms.openlocfilehash: 0da4e2168ccc7f5a62aa4265af3b7823dd4cb050
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689140"
---
# <span data-ttu-id="d1fa2-101">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d1fa2-101">Get-AzApiManagementPolicy</span></span>

## <span data-ttu-id="d1fa2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1fa2-102">SYNOPSIS</span></span>
<span data-ttu-id="d1fa2-103">지정 된 범위 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-103">Gets the specified scope policy.</span></span>

## <span data-ttu-id="d1fa2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d1fa2-104">SYNTAX</span></span>

### <span data-ttu-id="d1fa2-105">GetTenantLevel (기본값)</span><span class="sxs-lookup"><span data-stu-id="d1fa2-105">GetTenantLevel (Default)</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1fa2-106">Get제품 수준</span><span class="sxs-lookup"><span data-stu-id="d1fa2-106">GetProductLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d1fa2-107">GetApiLevel</span><span class="sxs-lookup"><span data-stu-id="d1fa2-107">GetApiLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1fa2-108">GetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="d1fa2-108">GetOperationLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] -OperationId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1fa2-109">설명은</span><span class="sxs-lookup"><span data-stu-id="d1fa2-109">DESCRIPTION</span></span>
<span data-ttu-id="d1fa2-110">**AzApiManagementPolicy** cmdlet은 지정 된 범위 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-110">The **Get-AzApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="d1fa2-111">예제의</span><span class="sxs-lookup"><span data-stu-id="d1fa2-111">EXAMPLES</span></span>

### <span data-ttu-id="d1fa2-112">예제 1: 테 넌 트 수준 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="d1fa2-112">Example 1: Get the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="d1fa2-113">이 명령은 테 넌 트 수준 정책을 가져와 tenantpolicy.xml 라는 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="d1fa2-114">예제 2: 제품 범위 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="d1fa2-114">Example 2: Get the product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="d1fa2-115">이 명령은 제품 범위 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="d1fa2-116">예제 3: API 범위 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="d1fa2-116">Example 3: Get the API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="d1fa2-117">이 명령은 API 범위 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="d1fa2-118">예제 4: 작업 범위 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="d1fa2-118">Example 4: Get the operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="d1fa2-119">이 명령은 작업 범위 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-119">This command gets the operation-scope policy.</span></span>

## <span data-ttu-id="d1fa2-120">변수</span><span class="sxs-lookup"><span data-stu-id="d1fa2-120">PARAMETERS</span></span>

### <span data-ttu-id="d1fa2-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d1fa2-121">-ApiId</span></span>
<span data-ttu-id="d1fa2-122">기존 API의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="d1fa2-123">이 매개 변수를 지정 하면 cmdlet이 API 범위 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-123">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

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

### <span data-ttu-id="d1fa2-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="d1fa2-124">-ApiRevision</span></span>
<span data-ttu-id="d1fa2-125">API 개정판의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-125">Identifier of API Revision.</span></span> <span data-ttu-id="d1fa2-126">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-126">This parameter is optional.</span></span> <span data-ttu-id="d1fa2-127">지정 하지 않으면 현재 활성 api 개정판에서 정책이 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-127">If not specified, the policy will be retrieved from the currently active api revision.</span></span>

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

### <span data-ttu-id="d1fa2-128">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="d1fa2-128">-Context</span></span>
<span data-ttu-id="d1fa2-129">**PsApiManagementContext** 의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-129">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="d1fa2-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1fa2-130">-DefaultProfile</span></span>
<span data-ttu-id="d1fa2-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1fa2-132">-Force</span><span class="sxs-lookup"><span data-stu-id="d1fa2-132">-Force</span></span>
<span data-ttu-id="d1fa2-133">ps_force</span><span class="sxs-lookup"><span data-stu-id="d1fa2-133">ps_force</span></span>

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

### <span data-ttu-id="d1fa2-134">-형식</span><span class="sxs-lookup"><span data-stu-id="d1fa2-134">-Format</span></span>
<span data-ttu-id="d1fa2-135">API 관리 정책의 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-135">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="d1fa2-136">이 매개 변수의 기본값은 "application/vnd. policy + xml"입니다.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-136">The default value for this parameter is "application/vnd.ms-az-apim.policy+xml".</span></span>

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

### <span data-ttu-id="d1fa2-137">-OperationId</span><span class="sxs-lookup"><span data-stu-id="d1fa2-137">-OperationId</span></span>
<span data-ttu-id="d1fa2-138">기존 API 작업의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-138">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="d1fa2-139">*Apiid* 에이 매개 변수를 지정 하는 경우 cmdlet은 작업 범위 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-139">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

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

### <span data-ttu-id="d1fa2-140">-ProductId</span><span class="sxs-lookup"><span data-stu-id="d1fa2-140">-ProductId</span></span>
<span data-ttu-id="d1fa2-141">기존 제품의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-141">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="d1fa2-142">이 매개 변수를 지정 하는 경우 cmdlet은 제품 범위 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-142">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

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

### <span data-ttu-id="d1fa2-143">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="d1fa2-143">-SaveAs</span></span>
<span data-ttu-id="d1fa2-144">결과를 저장할 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-144">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="d1fa2-145">이 매개 변수를 지정 하지 않으면 결과는 sting로 파이프라인 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-145">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="d1fa2-146">-확인</span><span class="sxs-lookup"><span data-stu-id="d1fa2-146">-Confirm</span></span>
<span data-ttu-id="d1fa2-147">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1fa2-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1fa2-148">-WhatIf</span></span>
<span data-ttu-id="d1fa2-149">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d1fa2-150">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1fa2-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1fa2-151">CommonParameters</span></span>
<span data-ttu-id="d1fa2-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1fa2-153">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1fa2-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1fa2-154">입력</span><span class="sxs-lookup"><span data-stu-id="d1fa2-154">INPUTS</span></span>

### <span data-ttu-id="d1fa2-155">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d1fa2-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d1fa2-156">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d1fa2-156">System.String</span></span>

### <span data-ttu-id="d1fa2-157">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d1fa2-157">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d1fa2-158">출력</span><span class="sxs-lookup"><span data-stu-id="d1fa2-158">OUTPUTS</span></span>

### <span data-ttu-id="d1fa2-159">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d1fa2-159">System.String</span></span>

## <span data-ttu-id="d1fa2-160">상속자</span><span class="sxs-lookup"><span data-stu-id="d1fa2-160">NOTES</span></span>

## <span data-ttu-id="d1fa2-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1fa2-161">RELATED LINKS</span></span>

[<span data-ttu-id="d1fa2-162">제거-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d1fa2-162">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)

[<span data-ttu-id="d1fa2-163">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d1fa2-163">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


