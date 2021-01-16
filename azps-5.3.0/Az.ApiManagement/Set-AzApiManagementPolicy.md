---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
ms.openlocfilehash: ee0a95653dbc949518c485554c6202664d943ba3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381655"
---
# <span data-ttu-id="a0644-101">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a0644-101">Set-AzApiManagementPolicy</span></span>

## <span data-ttu-id="a0644-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0644-102">SYNOPSIS</span></span>
<span data-ttu-id="a0644-103">API Management에 대해 지정된 범위 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a0644-103">Sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="a0644-104">구문</span><span class="sxs-lookup"><span data-stu-id="a0644-104">SYNTAX</span></span>

### <span data-ttu-id="a0644-105">SetTenantLevel(기본값)</span><span class="sxs-lookup"><span data-stu-id="a0644-105">SetTenantLevel (Default)</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a0644-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="a0644-106">SetProductLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0644-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="a0644-107">SetApiLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0644-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="a0644-108">SetOperationLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>]
 [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0644-109">설명</span><span class="sxs-lookup"><span data-stu-id="a0644-109">DESCRIPTION</span></span>
<span data-ttu-id="a0644-110">**Set-AzApiManagementPolicy** cmdlet은 API Management에 대해 지정된 범위 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a0644-110">The **Set-AzApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="a0644-111">예제</span><span class="sxs-lookup"><span data-stu-id="a0644-111">EXAMPLES</span></span>

### <span data-ttu-id="a0644-112">예제 1: 테넌트 수준 정책 설정</span><span class="sxs-lookup"><span data-stu-id="a0644-112">Example 1: Set the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="a0644-113">이 명령은 테넌트 수준 정책을 tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="a0644-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="a0644-114">예제 2: 제품 범위 정책 설정</span><span class="sxs-lookup"><span data-stu-id="a0644-114">Example 2: Set a product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="a0644-115">이 명령은 API Management에 대한 제품 범위 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a0644-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="a0644-116">예제 3: API 범위 정책 설정</span><span class="sxs-lookup"><span data-stu-id="a0644-116">Example 3: Set API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="a0644-117">이 명령은 API Management에 대한 API 범위 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a0644-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="a0644-118">예제 4: 작업 범위 정책 설정</span><span class="sxs-lookup"><span data-stu-id="a0644-118">Example 4: Set operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="a0644-119">이 명령은 API Management에 대한 작업 범위 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a0644-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="a0644-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0644-120">PARAMETERS</span></span>

### <span data-ttu-id="a0644-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a0644-121">-ApiId</span></span>
<span data-ttu-id="a0644-122">기존 API의 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a0644-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="a0644-123">이 매개 변수를 지정하는 경우 cmdlet은 API 범위 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a0644-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0644-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="a0644-124">-ApiRevision</span></span>
<span data-ttu-id="a0644-125">API 개정의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a0644-125">Identifier of API Revision.</span></span> <span data-ttu-id="a0644-126">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="a0644-126">This parameter is optional.</span></span> <span data-ttu-id="a0644-127">지정하지 않으면 현재 활성 API 버전에서 정책이 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0644-127">If not specified, the policy will be updated in the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0644-128">-Context</span><span class="sxs-lookup"><span data-stu-id="a0644-128">-Context</span></span>
<span data-ttu-id="a0644-129">**PsApiManagementContext의 인스턴스를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="a0644-129">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="a0644-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0644-130">-DefaultProfile</span></span>
<span data-ttu-id="a0644-131">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a0644-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0644-132">-Format</span><span class="sxs-lookup"><span data-stu-id="a0644-132">-Format</span></span>
<span data-ttu-id="a0644-133">정책의 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a0644-133">Specifies the format of the policy.</span></span> <span data-ttu-id="a0644-134">사용하는 경우 정책 내에 포함된 식은 `application/vnd.ms-azure-apim.policy+xml` XML 이스케이프되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0644-134">When using `application/vnd.ms-azure-apim.policy+xml`, expressions contained within the policy must be XML-escaped.</span></span> <span data-ttu-id="a0644-135">사용하는 `application/vnd.ms-azure-apim.policy.raw+xml` 경우  정책이 XML 이스케이프될 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a0644-135">When using `application/vnd.ms-azure-apim.policy.raw+xml` it is **not** necessary for the policy to be XML-escaped.</span></span>
<span data-ttu-id="a0644-136">기본값은 `application/vnd.ms-azure-apim.policy+xml` .</span><span class="sxs-lookup"><span data-stu-id="a0644-136">The default value is `application/vnd.ms-azure-apim.policy+xml`.</span></span>
<span data-ttu-id="a0644-137">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="a0644-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="a0644-138">-OperationId</span><span class="sxs-lookup"><span data-stu-id="a0644-138">-OperationId</span></span>
<span data-ttu-id="a0644-139">기존 작업의 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a0644-139">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="a0644-140">ApiId로 지정된 경우 작업 범위 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a0644-140">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="a0644-141">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="a0644-141">This parameters is required.</span></span>

```yaml
Type: System.String
Parameter Sets: SetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0644-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0644-142">-PassThru</span></span>
<span data-ttu-id="a0644-143">passthru</span><span class="sxs-lookup"><span data-stu-id="a0644-143">passthru</span></span>

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

### <span data-ttu-id="a0644-144">-Policy</span><span class="sxs-lookup"><span data-stu-id="a0644-144">-Policy</span></span>
<span data-ttu-id="a0644-145">정책 문서를 문자열로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a0644-145">Specifies the policy document as a string.</span></span>
<span data-ttu-id="a0644-146">*PolicyFilePath가* 지정되지 않은 경우 이 매개 변수가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="a0644-146">This parameter is required if the -*PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="a0644-147">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="a0644-147">-PolicyFilePath</span></span>
<span data-ttu-id="a0644-148">정책 문서 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a0644-148">Specifies the policy document file path.</span></span>
<span data-ttu-id="a0644-149">Policy 매개 변수를 지정하지 *않은* 경우 이 매개 변수가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="a0644-149">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="a0644-150">-PolicyUrl</span><span class="sxs-lookup"><span data-stu-id="a0644-150">-PolicyUrl</span></span>
<span data-ttu-id="a0644-151">정책 문서가 호스팅되는 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="a0644-151">The Url where the Policy document is hosted.</span></span> <span data-ttu-id="a0644-152">-Policy 또는 -PolicyFilePath가 지정되지 않은 경우 이 매개 변수가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="a0644-152">This parameter is required if -Policy or -PolicyFilePath is not specified.</span></span>

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

### <span data-ttu-id="a0644-153">-ProductId</span><span class="sxs-lookup"><span data-stu-id="a0644-153">-ProductId</span></span>
<span data-ttu-id="a0644-154">기존 제품의 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a0644-154">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="a0644-155">이 매개 변수를 지정하는 경우 cmdlet은 제품 범위 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a0644-155">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0644-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0644-156">CommonParameters</span></span>
<span data-ttu-id="a0644-157">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a0644-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0644-158">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a0644-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0644-159">입력</span><span class="sxs-lookup"><span data-stu-id="a0644-159">INPUTS</span></span>

### <span data-ttu-id="a0644-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a0644-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a0644-161">System.String</span><span class="sxs-lookup"><span data-stu-id="a0644-161">System.String</span></span>

### <span data-ttu-id="a0644-162">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a0644-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a0644-163">출력</span><span class="sxs-lookup"><span data-stu-id="a0644-163">OUTPUTS</span></span>

### <span data-ttu-id="a0644-164">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a0644-164">System.Boolean</span></span>

## <span data-ttu-id="a0644-165">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a0644-165">NOTES</span></span>

## <span data-ttu-id="a0644-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a0644-166">RELATED LINKS</span></span>

[<span data-ttu-id="a0644-167">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a0644-167">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="a0644-168">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a0644-168">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)


