---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiVersionSet.md
ms.openlocfilehash: 4ff48709b02cdd0270c559ea8be2f4e269dbce2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93701994"
---
# <span data-ttu-id="357d8-101">Remove-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="357d8-101">Remove-AzureRmApiManagementApiVersionSet</span></span>

## <span data-ttu-id="357d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="357d8-102">SYNOPSIS</span></span>
<span data-ttu-id="357d8-103">특정 Api 버전 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="357d8-103">Removes a particular Api Version Set</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="357d8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="357d8-104">SYNTAX</span></span>

### <span data-ttu-id="357d8-105">ExpandedParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="357d8-105">ExpandedParameter (Default)</span></span>
```
Remove-AzureRmApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="357d8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="357d8-106">ByInputObject</span></span>
```
Remove-AzureRmApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="357d8-107">설명은</span><span class="sxs-lookup"><span data-stu-id="357d8-107">DESCRIPTION</span></span>

<span data-ttu-id="357d8-108">**AzureRmApiManagementApiVersionSet** cmdlet은 기존 API 버전 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="357d8-108">The **Remove-AzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="357d8-109">예제의</span><span class="sxs-lookup"><span data-stu-id="357d8-109">EXAMPLES</span></span>

### <span data-ttu-id="357d8-110">예제 1: API 버전 집합 제거</span><span class="sxs-lookup"><span data-stu-id="357d8-110">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="357d8-111">이 명령은 지정 된 ApiVersionSetId를 사용 하 여 API 버전 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="357d8-111">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="357d8-112">변수</span><span class="sxs-lookup"><span data-stu-id="357d8-112">PARAMETERS</span></span>

### <span data-ttu-id="357d8-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="357d8-113">-ApiVersionSetId</span></span>
<span data-ttu-id="357d8-114">API 버전 집합의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="357d8-114">Identifier of the API Version Set.</span></span>
<span data-ttu-id="357d8-115">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="357d8-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="357d8-116">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="357d8-116">-Context</span></span>
<span data-ttu-id="357d8-117">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="357d8-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="357d8-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="357d8-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="357d8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="357d8-119">-DefaultProfile</span></span>
<span data-ttu-id="357d8-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="357d8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="357d8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="357d8-121">-InputObject</span></span>
<span data-ttu-id="357d8-122">PsApiManagementApiVersionSet의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="357d8-122">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="357d8-123">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="357d8-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="357d8-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="357d8-124">-PassThru</span></span>
<span data-ttu-id="357d8-125">지정 된 경우 대/소문자 구분 작업이 성공한 경우 true를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="357d8-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="357d8-126">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="357d8-126">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="357d8-127">-확인</span><span class="sxs-lookup"><span data-stu-id="357d8-127">-Confirm</span></span>
<span data-ttu-id="357d8-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="357d8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="357d8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="357d8-129">-WhatIf</span></span>
<span data-ttu-id="357d8-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="357d8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="357d8-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="357d8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="357d8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="357d8-132">CommonParameters</span></span>
<span data-ttu-id="357d8-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="357d8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="357d8-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="357d8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="357d8-135">입력</span><span class="sxs-lookup"><span data-stu-id="357d8-135">INPUTS</span></span>

### <span data-ttu-id="357d8-136">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="357d8-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="357d8-137">매개 변수: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="357d8-137">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="357d8-138">ApiManagement. ServiceManagement. \ PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="357d8-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>
<span data-ttu-id="357d8-139">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="357d8-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="357d8-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="357d8-140">System.String</span></span>

## <span data-ttu-id="357d8-141">출력</span><span class="sxs-lookup"><span data-stu-id="357d8-141">OUTPUTS</span></span>

### <span data-ttu-id="357d8-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="357d8-142">System.Boolean</span></span>

## <span data-ttu-id="357d8-143">상속자</span><span class="sxs-lookup"><span data-stu-id="357d8-143">NOTES</span></span>

## <span data-ttu-id="357d8-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="357d8-144">RELATED LINKS</span></span>

[<span data-ttu-id="357d8-145">Get-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="357d8-145">Get-AzureRmApiManagementApiVersionSet</span></span>](./Get-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="357d8-146">새로운 AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="357d8-146">New-AzureRmApiManagementApiVersionSet</span></span>](./New-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="357d8-147">Set-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="357d8-147">Set-AzureRmApiManagementApiVersionSet</span></span>](./Set-AzureRmApiManagementApiVersionSet.md)
