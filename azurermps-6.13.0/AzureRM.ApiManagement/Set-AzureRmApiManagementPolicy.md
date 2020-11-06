---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 75bb963195244a5a1a27ca004eb2795b6b5bb556
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526388"
---
# <span data-ttu-id="9a514-101">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="9a514-101">Set-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="9a514-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a514-102">SYNOPSIS</span></span>
<span data-ttu-id="9a514-103">API Management에 대해 지정 된 범위 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a514-103">Sets the specified scope policy for API Management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a514-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9a514-104">SYNTAX</span></span>

### <span data-ttu-id="9a514-105">Setten앤틸리스 수준 (기본값)</span><span class="sxs-lookup"><span data-stu-id="9a514-105">SetTenantLevel (Default)</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9a514-106">Set제품 수준</span><span class="sxs-lookup"><span data-stu-id="9a514-106">SetProductLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a514-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="9a514-107">SetApiLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a514-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="9a514-108">SetOperationLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>]
 [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a514-109">설명은</span><span class="sxs-lookup"><span data-stu-id="9a514-109">DESCRIPTION</span></span>
<span data-ttu-id="9a514-110">**AzureRmApiManagementPolicy** CMDLET은 API Management에 대해 지정 된 범위 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a514-110">The **Set-AzureRmApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="9a514-111">예제의</span><span class="sxs-lookup"><span data-stu-id="9a514-111">EXAMPLES</span></span>

### <span data-ttu-id="9a514-112">예제 1: 테 넌 트 수준 정책 설정</span><span class="sxs-lookup"><span data-stu-id="9a514-112">Example 1: Set the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="9a514-113">이 명령은 tenantpolicy.xml 라는 파일에서 테 넌 트 수준 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a514-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="9a514-114">예제 2: 제품 범위 정책 설정</span><span class="sxs-lookup"><span data-stu-id="9a514-114">Example 2: Set a product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="9a514-115">이 명령은 API Management에 대 한 제품 범위 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a514-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="9a514-116">예제 3: API 범위 정책 설정</span><span class="sxs-lookup"><span data-stu-id="9a514-116">Example 3: Set API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="9a514-117">이 명령은 API Management에 대 한 API 범위 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a514-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="9a514-118">예제 4: Set 작업 범위 정책</span><span class="sxs-lookup"><span data-stu-id="9a514-118">Example 4: Set operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="9a514-119">이 명령은 API Management에 대 한 작업 범위 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a514-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="9a514-120">변수</span><span class="sxs-lookup"><span data-stu-id="9a514-120">PARAMETERS</span></span>

### <span data-ttu-id="9a514-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9a514-121">-ApiId</span></span>
<span data-ttu-id="9a514-122">기존 API의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a514-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="9a514-123">이 매개 변수를 지정 하는 경우 cmdlet은 API 범위 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a514-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

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

### <span data-ttu-id="9a514-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="9a514-124">-ApiRevision</span></span>
<span data-ttu-id="9a514-125">API 개정판의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="9a514-125">Identifier of API Revision.</span></span> <span data-ttu-id="9a514-126">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="9a514-126">This parameter is optional.</span></span> <span data-ttu-id="9a514-127">지정 하지 않으면 정책이 현재 활성 api 개정판에서 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a514-127">If not specified, the policy will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="9a514-128">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="9a514-128">-Context</span></span>
<span data-ttu-id="9a514-129">**PsApiManagementContext** 의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a514-129">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="9a514-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a514-130">-DefaultProfile</span></span>
<span data-ttu-id="9a514-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9a514-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a514-132">-형식</span><span class="sxs-lookup"><span data-stu-id="9a514-132">-Format</span></span>
<span data-ttu-id="9a514-133">정책의 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a514-133">Specifies the format of the policy.</span></span> <span data-ttu-id="9a514-134">사용 하 `application/vnd.ms-azure-apim.policy+xml` 는 경우 정책에 포함 된 식은 XML 이스케이프 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a514-134">When using `application/vnd.ms-azure-apim.policy+xml`, expressions contained within the policy must be XML-escaped.</span></span> <span data-ttu-id="9a514-135">사용 하는 경우 `application/vnd.ms-azure-apim.policy.raw+xml` 정책이 XML로 이스케이프 될 필요는 **없습니다** .</span><span class="sxs-lookup"><span data-stu-id="9a514-135">When using `application/vnd.ms-azure-apim.policy.raw+xml` it is **not** necessary for the policy to be XML-escaped.</span></span>
<span data-ttu-id="9a514-136">기본값은 `application/vnd.ms-azure-apim.policy+xml` 입니다.</span><span class="sxs-lookup"><span data-stu-id="9a514-136">The default value is `application/vnd.ms-azure-apim.policy+xml`.</span></span>
<span data-ttu-id="9a514-137">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="9a514-137">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: application/vnd.ms-azure-apim.policy.raw+xml, application/vnd.ms-azure-apim.policy+xml

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a514-138">-OperationId</span><span class="sxs-lookup"><span data-stu-id="9a514-138">-OperationId</span></span>
<span data-ttu-id="9a514-139">기존 작업의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a514-139">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="9a514-140">ApiId를 사용 하 여 지정 하면 작업 범위 정책이 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a514-140">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="9a514-141">이 매개 변수는 필수 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="9a514-141">This parameters is required.</span></span>

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

### <span data-ttu-id="9a514-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a514-142">-PassThru</span></span>
<span data-ttu-id="9a514-143">passthru</span><span class="sxs-lookup"><span data-stu-id="9a514-143">passthru</span></span>

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

### <span data-ttu-id="9a514-144">-정책</span><span class="sxs-lookup"><span data-stu-id="9a514-144">-Policy</span></span>
<span data-ttu-id="9a514-145">정책 문서를 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a514-145">Specifies the policy document as a string.</span></span>
<span data-ttu-id="9a514-146">이 매개 변수는- *Policyfilepath* 가 지정 되지 않은 경우에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a514-146">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="9a514-147">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="9a514-147">-PolicyFilePath</span></span>
<span data-ttu-id="9a514-148">정책 문서 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a514-148">Specifies the policy document file path.</span></span>
<span data-ttu-id="9a514-149">이 매개 변수는 *정책* 매개 변수를 지정 하지 않은 경우에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a514-149">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="9a514-150">-PolicyUrl</span><span class="sxs-lookup"><span data-stu-id="9a514-150">-PolicyUrl</span></span>
<span data-ttu-id="9a514-151">정책 문서가 호스팅되는 Url입니다.</span><span class="sxs-lookup"><span data-stu-id="9a514-151">The Url where the Policy document is hosted.</span></span> <span data-ttu-id="9a514-152">-Policy 또는-PolicyFilePath가 지정 되지 않은 경우이 매개 변수가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a514-152">This parameter is required if -Policy or -PolicyFilePath is not specified.</span></span>

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

### <span data-ttu-id="9a514-153">-ProductId</span><span class="sxs-lookup"><span data-stu-id="9a514-153">-ProductId</span></span>
<span data-ttu-id="9a514-154">기존 제품의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a514-154">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="9a514-155">이 매개 변수를 지정 하면 cmdlet은 제품 범위 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a514-155">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

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

### <span data-ttu-id="9a514-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a514-156">CommonParameters</span></span>
<span data-ttu-id="9a514-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a514-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a514-158">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a514-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a514-159">입력</span><span class="sxs-lookup"><span data-stu-id="9a514-159">INPUTS</span></span>

### <span data-ttu-id="9a514-160">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9a514-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9a514-161">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9a514-161">System.String</span></span>

### <span data-ttu-id="9a514-162">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="9a514-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9a514-163">출력</span><span class="sxs-lookup"><span data-stu-id="9a514-163">OUTPUTS</span></span>

### <span data-ttu-id="9a514-164">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="9a514-164">System.Boolean</span></span>

## <span data-ttu-id="9a514-165">상속자</span><span class="sxs-lookup"><span data-stu-id="9a514-165">NOTES</span></span>

## <span data-ttu-id="9a514-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a514-166">RELATED LINKS</span></span>

[<span data-ttu-id="9a514-167">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="9a514-167">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="9a514-168">제거-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="9a514-168">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)


