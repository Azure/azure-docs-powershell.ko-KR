---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: 5b863c0d0c808c8cb993e4f78f9767d13fb634d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526363"
---
# <span data-ttu-id="ccbcf-101">Update-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="ccbcf-101">Update-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="ccbcf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccbcf-102">SYNOPSIS</span></span>
<span data-ttu-id="ccbcf-103">특정 Api 릴리스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccbcf-103">Updates a particular Api Release.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccbcf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ccbcf-104">SYNTAX</span></span>

### <span data-ttu-id="ccbcf-105">ExpandedParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="ccbcf-105">ExpandedParameter (Default)</span></span>
```
Update-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ReleaseId <String> -ApiId <String>
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ccbcf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ccbcf-106">ByInputObject</span></span>
```
Update-AzureRmApiManagementApiRelease [-Note <String>] -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccbcf-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ccbcf-107">DESCRIPTION</span></span>
<span data-ttu-id="ccbcf-108">**업데이트 AzureRmApiManagementApiRelease** Cmdlet은 Azure API Management api 릴리스를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccbcf-108">The **Update-AzureRmApiManagementApiRelease** cmdlet modifies an Azure API Management API Release.</span></span>

## <span data-ttu-id="ccbcf-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ccbcf-109">EXAMPLES</span></span>

### <span data-ttu-id="ccbcf-110">예제 1: API 개정판에 대 한 API 릴리스 업데이트</span><span class="sxs-lookup"><span data-stu-id="ccbcf-110">Example 1: Updates an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzureRmApiManagementApiRelease -Context $ApiMgmtContext -ApiId "echo-api" -ReleaseId "echo-api-release" -Note "Releasing version 2 of the echo-api to public"
```

<span data-ttu-id="ccbcf-111">이 명령은 `echo-api-release` api의 Api 릴리스를 `echo-api` 새 메모로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccbcf-111">This command updates the `echo-api-release` API Release of the Api `echo-api` with new note.</span></span>

## <span data-ttu-id="ccbcf-112">변수</span><span class="sxs-lookup"><span data-stu-id="ccbcf-112">PARAMETERS</span></span>

### <span data-ttu-id="ccbcf-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ccbcf-113">-ApiId</span></span>
<span data-ttu-id="ccbcf-114">기존 API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="ccbcf-114">Identifier of existing API.</span></span>
<span data-ttu-id="ccbcf-115">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="ccbcf-115">This parameter is required.</span></span>

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

### <span data-ttu-id="ccbcf-116">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="ccbcf-116">-Context</span></span>
<span data-ttu-id="ccbcf-117">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="ccbcf-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ccbcf-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="ccbcf-118">This parameter is required.</span></span>

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

### <span data-ttu-id="ccbcf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccbcf-119">-DefaultProfile</span></span>
<span data-ttu-id="ccbcf-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ccbcf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccbcf-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ccbcf-121">-InputObject</span></span>
<span data-ttu-id="ccbcf-122">ApiManagement. ServiceManagement의 인스턴스를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccbcf-122">Instance of type Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccbcf-123">-메모</span><span class="sxs-lookup"><span data-stu-id="ccbcf-123">-Note</span></span>
<span data-ttu-id="ccbcf-124">Api 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="ccbcf-124">Api Release Notes.</span></span>
<span data-ttu-id="ccbcf-125">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="ccbcf-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="ccbcf-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ccbcf-126">-PassThru</span></span>
<span data-ttu-id="ccbcf-127">지정 된 경우 set API Release를 나타내는 ApiManagement의 인스턴스를 ServiceManagement. PsApiManagementApiRelease 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="ccbcf-127">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease type representing the set API Release.</span></span>

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

### <span data-ttu-id="ccbcf-128">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="ccbcf-128">-ReleaseId</span></span>
<span data-ttu-id="ccbcf-129">Api 개정판 ReleaseId에 대 한 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="ccbcf-129">Identifier for the Api Revision ReleaseId.</span></span>
<span data-ttu-id="ccbcf-130">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="ccbcf-130">This parameter is required.</span></span>

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

### <span data-ttu-id="ccbcf-131">-확인</span><span class="sxs-lookup"><span data-stu-id="ccbcf-131">-Confirm</span></span>
<span data-ttu-id="ccbcf-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccbcf-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccbcf-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccbcf-133">-WhatIf</span></span>
<span data-ttu-id="ccbcf-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ccbcf-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccbcf-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ccbcf-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccbcf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccbcf-136">CommonParameters</span></span>
<span data-ttu-id="ccbcf-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccbcf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccbcf-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccbcf-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccbcf-139">입력</span><span class="sxs-lookup"><span data-stu-id="ccbcf-139">INPUTS</span></span>

### <span data-ttu-id="ccbcf-140">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ccbcf-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="ccbcf-141">매개 변수: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ccbcf-141">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="ccbcf-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ccbcf-142">System.String</span></span>

### <span data-ttu-id="ccbcf-143">ApiManagement. ServiceManagement. \ PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="ccbcf-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="ccbcf-144">출력</span><span class="sxs-lookup"><span data-stu-id="ccbcf-144">OUTPUTS</span></span>

### <span data-ttu-id="ccbcf-145">ApiManagement. ServiceManagement. \ PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="ccbcf-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="ccbcf-146">상속자</span><span class="sxs-lookup"><span data-stu-id="ccbcf-146">NOTES</span></span>

## <span data-ttu-id="ccbcf-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ccbcf-147">RELATED LINKS</span></span>

[<span data-ttu-id="ccbcf-148">Get-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="ccbcf-148">Get-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="ccbcf-149">새로운 AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="ccbcf-149">New-AzureRmApiManagementApiRelease</span></span>](./New-AzureRmApiManagementApiRelease.md)
