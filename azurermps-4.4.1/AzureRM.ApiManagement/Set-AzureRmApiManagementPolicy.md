---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 8073df3946f5bf42ee8b0e5f2c7ae7881e905eaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531249"
---
# <span data-ttu-id="59907-101">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="59907-101">Set-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="59907-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59907-102">SYNOPSIS</span></span>
<span data-ttu-id="59907-103">API Management에 대해 지정 된 범위 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59907-103">Sets the specified scope policy for API Management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59907-104">구문과</span><span class="sxs-lookup"><span data-stu-id="59907-104">SYNTAX</span></span>

### <span data-ttu-id="59907-105">테 넌 트 수준 (기본값)</span><span class="sxs-lookup"><span data-stu-id="59907-105">Tenant level (Default)</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59907-106">제품 수준</span><span class="sxs-lookup"><span data-stu-id="59907-106">Product level</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59907-107">API 수준</span><span class="sxs-lookup"><span data-stu-id="59907-107">API level</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59907-108">작업 수준</span><span class="sxs-lookup"><span data-stu-id="59907-108">Operation level</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59907-109">설명은</span><span class="sxs-lookup"><span data-stu-id="59907-109">DESCRIPTION</span></span>
<span data-ttu-id="59907-110">**AzureRmApiManagementPolicy** CMDLET은 API Management에 대해 지정 된 범위 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59907-110">The **Set-AzureRmApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="59907-111">예제의</span><span class="sxs-lookup"><span data-stu-id="59907-111">EXAMPLES</span></span>

### <span data-ttu-id="59907-112">예제 1: 테 넌 트 수준 정책 설정</span><span class="sxs-lookup"><span data-stu-id="59907-112">Example 1: Set the tenant level policy</span></span>
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="59907-113">이 명령은 tenantpolicy.xml 라는 파일에서 테 넌 트 수준 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59907-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="59907-114">예제 2: 제품 범위 정책 설정</span><span class="sxs-lookup"><span data-stu-id="59907-114">Example 2: Set a product-scope policy</span></span>
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="59907-115">이 명령은 API Management에 대 한 제품 범위 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59907-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="59907-116">예제 3: API 범위 정책 설정</span><span class="sxs-lookup"><span data-stu-id="59907-116">Example 3: Set API-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="59907-117">이 명령은 API Management에 대 한 API 범위 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59907-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="59907-118">예제 4: Set 작업 범위 정책</span><span class="sxs-lookup"><span data-stu-id="59907-118">Example 4: Set operation-scope policy</span></span>
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="59907-119">이 명령은 API Management에 대 한 작업 범위 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59907-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="59907-120">변수</span><span class="sxs-lookup"><span data-stu-id="59907-120">PARAMETERS</span></span>

### <span data-ttu-id="59907-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="59907-121">-ApiId</span></span>
<span data-ttu-id="59907-122">기존 API의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59907-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="59907-123">이 매개 변수를 지정 하는 경우 cmdlet은 API 범위 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59907-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

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

### <span data-ttu-id="59907-124">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="59907-124">-Context</span></span>
<span data-ttu-id="59907-125">**PsApiManagementContext** 의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59907-125">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="59907-126">-형식</span><span class="sxs-lookup"><span data-stu-id="59907-126">-Format</span></span>
<span data-ttu-id="59907-127">정책의 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59907-127">Specifies the format of the policy.</span></span>
<span data-ttu-id="59907-128">기본값은 "application/vnd ms-azure-apim. policy + xml"입니다.</span><span class="sxs-lookup"><span data-stu-id="59907-128">The default value is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="59907-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="59907-129">-OperationId</span></span>
<span data-ttu-id="59907-130">기존 작업의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59907-130">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="59907-131">ApiId를 사용 하 여 지정 하면 작업 범위 정책이 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="59907-131">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="59907-132">이 매개 변수는 필수 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="59907-132">This parameters is required.</span></span>

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

### <span data-ttu-id="59907-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59907-133">-PassThru</span></span>
<span data-ttu-id="59907-134">passthru</span><span class="sxs-lookup"><span data-stu-id="59907-134">passthru</span></span>

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

### <span data-ttu-id="59907-135">-정책</span><span class="sxs-lookup"><span data-stu-id="59907-135">-Policy</span></span>
<span data-ttu-id="59907-136">정책 문서를 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59907-136">Specifies the policy document as a string.</span></span>
<span data-ttu-id="59907-137">이 매개 변수는- *Policyfilepath* 가 지정 되지 않은 경우에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="59907-137">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="59907-138">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="59907-138">-PolicyFilePath</span></span>
<span data-ttu-id="59907-139">정책 문서 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59907-139">Specifies the policy document file path.</span></span>
<span data-ttu-id="59907-140">이 매개 변수는 *정책* 매개 변수를 지정 하지 않은 경우에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="59907-140">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="59907-141">-ProductId</span><span class="sxs-lookup"><span data-stu-id="59907-141">-ProductId</span></span>
<span data-ttu-id="59907-142">기존 제품의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59907-142">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="59907-143">이 매개 변수를 지정 하면 cmdlet은 제품 범위 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59907-143">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

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

### <span data-ttu-id="59907-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59907-144">-DefaultProfile</span></span>
<span data-ttu-id="59907-145">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="59907-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59907-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59907-146">CommonParameters</span></span>
<span data-ttu-id="59907-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="59907-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59907-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59907-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59907-149">입력</span><span class="sxs-lookup"><span data-stu-id="59907-149">INPUTS</span></span>

## <span data-ttu-id="59907-150">출력</span><span class="sxs-lookup"><span data-stu-id="59907-150">OUTPUTS</span></span>

### <span data-ttu-id="59907-151">부울</span><span class="sxs-lookup"><span data-stu-id="59907-151">bool</span></span>

## <span data-ttu-id="59907-152">상속자</span><span class="sxs-lookup"><span data-stu-id="59907-152">NOTES</span></span>

## <span data-ttu-id="59907-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59907-153">RELATED LINKS</span></span>

[<span data-ttu-id="59907-154">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="59907-154">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="59907-155">제거-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="59907-155">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)


