---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 0f9ee1c2190dbc3d657ecc52cd85b6af8b0cac4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702660"
---
# <span data-ttu-id="ecb8c-101">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ecb8c-101">Set-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="ecb8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecb8c-102">SYNOPSIS</span></span>
<span data-ttu-id="ecb8c-103">API Management에 대해 지정 된 범위 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb8c-103">Sets the specified scope policy for API Management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecb8c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ecb8c-104">SYNTAX</span></span>

### <span data-ttu-id="ecb8c-105">Setten앤틸리스 수준 (기본값)</span><span class="sxs-lookup"><span data-stu-id="ecb8c-105">SetTenantLevel (Default)</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecb8c-106">Set제품 수준</span><span class="sxs-lookup"><span data-stu-id="ecb8c-106">SetProductLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ecb8c-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="ecb8c-107">SetApiLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ecb8c-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="ecb8c-108">SetOperationLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecb8c-109">설명은</span><span class="sxs-lookup"><span data-stu-id="ecb8c-109">DESCRIPTION</span></span>
<span data-ttu-id="ecb8c-110">**AzureRmApiManagementPolicy** CMDLET은 API Management에 대해 지정 된 범위 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb8c-110">The **Set-AzureRmApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="ecb8c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="ecb8c-111">EXAMPLES</span></span>

### <span data-ttu-id="ecb8c-112">예제 1: 테 넌 트 수준 정책 설정</span><span class="sxs-lookup"><span data-stu-id="ecb8c-112">Example 1: Set the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="ecb8c-113">이 명령은 tenantpolicy.xml 라는 파일에서 테 넌 트 수준 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb8c-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="ecb8c-114">예제 2: 제품 범위 정책 설정</span><span class="sxs-lookup"><span data-stu-id="ecb8c-114">Example 2: Set a product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="ecb8c-115">이 명령은 API Management에 대 한 제품 범위 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb8c-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="ecb8c-116">예제 3: API 범위 정책 설정</span><span class="sxs-lookup"><span data-stu-id="ecb8c-116">Example 3: Set API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="ecb8c-117">이 명령은 API Management에 대 한 API 범위 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb8c-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="ecb8c-118">예제 4: Set 작업 범위 정책</span><span class="sxs-lookup"><span data-stu-id="ecb8c-118">Example 4: Set operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="ecb8c-119">이 명령은 API Management에 대 한 작업 범위 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb8c-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="ecb8c-120">변수</span><span class="sxs-lookup"><span data-stu-id="ecb8c-120">PARAMETERS</span></span>

### <span data-ttu-id="ecb8c-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ecb8c-121">-ApiId</span></span>
<span data-ttu-id="ecb8c-122">기존 API의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb8c-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="ecb8c-123">이 매개 변수를 지정 하는 경우 cmdlet은 API 범위 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb8c-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecb8c-124">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="ecb8c-124">-Context</span></span>
<span data-ttu-id="ecb8c-125">**PsApiManagementContext** 의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb8c-125">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="ecb8c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecb8c-126">-DefaultProfile</span></span>
<span data-ttu-id="ecb8c-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb8c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="ecb8c-128">-형식</span><span class="sxs-lookup"><span data-stu-id="ecb8c-128">-Format</span></span>
<span data-ttu-id="ecb8c-129">정책의 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb8c-129">Specifies the format of the policy.</span></span>
<span data-ttu-id="ecb8c-130">기본값은 "application/vnd ms-azure-apim. policy + xml"입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb8c-130">The default value is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="ecb8c-131">-OperationId</span><span class="sxs-lookup"><span data-stu-id="ecb8c-131">-OperationId</span></span>
<span data-ttu-id="ecb8c-132">기존 작업의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb8c-132">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="ecb8c-133">ApiId를 사용 하 여 지정 하면 작업 범위 정책이 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecb8c-133">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="ecb8c-134">이 매개 변수는 필수 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb8c-134">This parameters is required.</span></span>

```yaml
Type: String
Parameter Sets: SetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecb8c-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ecb8c-135">-PassThru</span></span>
<span data-ttu-id="ecb8c-136">passthru</span><span class="sxs-lookup"><span data-stu-id="ecb8c-136">passthru</span></span>

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

### <span data-ttu-id="ecb8c-137">-정책</span><span class="sxs-lookup"><span data-stu-id="ecb8c-137">-Policy</span></span>
<span data-ttu-id="ecb8c-138">정책 문서를 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb8c-138">Specifies the policy document as a string.</span></span>
<span data-ttu-id="ecb8c-139">이 매개 변수는- *Policyfilepath* 가 지정 되지 않은 경우에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb8c-139">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="ecb8c-140">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="ecb8c-140">-PolicyFilePath</span></span>
<span data-ttu-id="ecb8c-141">정책 문서 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb8c-141">Specifies the policy document file path.</span></span>
<span data-ttu-id="ecb8c-142">이 매개 변수는 *정책* 매개 변수를 지정 하지 않은 경우에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb8c-142">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="ecb8c-143">-ProductId</span><span class="sxs-lookup"><span data-stu-id="ecb8c-143">-ProductId</span></span>
<span data-ttu-id="ecb8c-144">기존 제품의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb8c-144">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="ecb8c-145">이 매개 변수를 지정 하면 cmdlet은 제품 범위 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb8c-145">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: SetProductLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecb8c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecb8c-146">CommonParameters</span></span>
<span data-ttu-id="ecb8c-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb8c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecb8c-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecb8c-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecb8c-149">입력</span><span class="sxs-lookup"><span data-stu-id="ecb8c-149">INPUTS</span></span>

### <span data-ttu-id="ecb8c-150">않아야</span><span class="sxs-lookup"><span data-stu-id="ecb8c-150">None</span></span>
<span data-ttu-id="ecb8c-151">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ecb8c-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ecb8c-152">출력</span><span class="sxs-lookup"><span data-stu-id="ecb8c-152">OUTPUTS</span></span>

### <span data-ttu-id="ecb8c-153">부울</span><span class="sxs-lookup"><span data-stu-id="ecb8c-153">bool</span></span>

## <span data-ttu-id="ecb8c-154">상속자</span><span class="sxs-lookup"><span data-stu-id="ecb8c-154">NOTES</span></span>

## <span data-ttu-id="ecb8c-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ecb8c-155">RELATED LINKS</span></span>

[<span data-ttu-id="ecb8c-156">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ecb8c-156">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="ecb8c-157">제거-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ecb8c-157">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)


