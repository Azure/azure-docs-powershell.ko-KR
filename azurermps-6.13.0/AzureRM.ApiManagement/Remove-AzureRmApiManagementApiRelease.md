---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: 71256ab72d8c5c6042aa6c17b184066f96b3a813
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524727"
---
# <span data-ttu-id="d9fb5-101">Remove-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="d9fb5-101">Remove-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="d9fb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9fb5-102">SYNOPSIS</span></span>
<span data-ttu-id="d9fb5-103">특정 API 릴리스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9fb5-103">Removes a particular API Release</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9fb5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d9fb5-104">SYNTAX</span></span>

### <span data-ttu-id="d9fb5-105">ByApiReleaseId (기본값)</span><span class="sxs-lookup"><span data-stu-id="d9fb5-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9fb5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d9fb5-106">ByInputObject</span></span>
```
Remove-AzureRmApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9fb5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d9fb5-107">DESCRIPTION</span></span>

<span data-ttu-id="d9fb5-108">**AzureRmApiManagementApiRelease** cmdlet은 기존 API 릴리스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9fb5-108">The **Remove-AzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="d9fb5-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d9fb5-109">EXAMPLES</span></span>

### <span data-ttu-id="d9fb5-110">예제 1: API 릴리스 제거</span><span class="sxs-lookup"><span data-stu-id="d9fb5-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="d9fb5-111">이 명령은 지정 된 ApiId 및 ReleaseId를 사용 하 여 API Release를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9fb5-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="d9fb5-112">변수</span><span class="sxs-lookup"><span data-stu-id="d9fb5-112">PARAMETERS</span></span>

### <span data-ttu-id="d9fb5-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d9fb5-113">-ApiId</span></span>
<span data-ttu-id="d9fb5-114">API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="d9fb5-114">Identifier of the API.</span></span>
<span data-ttu-id="d9fb5-115">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="d9fb5-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9fb5-116">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="d9fb5-116">-Context</span></span>
<span data-ttu-id="d9fb5-117">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="d9fb5-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d9fb5-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="d9fb5-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9fb5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9fb5-119">-DefaultProfile</span></span>
<span data-ttu-id="d9fb5-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d9fb5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9fb5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9fb5-121">-InputObject</span></span>
<span data-ttu-id="d9fb5-122">PsApiManagementApiRelease의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="d9fb5-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="d9fb5-123">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="d9fb5-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9fb5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9fb5-124">-PassThru</span></span>
<span data-ttu-id="d9fb5-125">지정 된 경우 대/소문자 구분 작업이 성공한 경우 true를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="d9fb5-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="d9fb5-126">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="d9fb5-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="d9fb5-127">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="d9fb5-127">-ReleaseId</span></span>
<span data-ttu-id="d9fb5-128">API 릴리스의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="d9fb5-128">Identifier of the API Release.</span></span>
<span data-ttu-id="d9fb5-129">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="d9fb5-129">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9fb5-130">-확인</span><span class="sxs-lookup"><span data-stu-id="d9fb5-130">-Confirm</span></span>
<span data-ttu-id="d9fb5-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9fb5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9fb5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9fb5-132">-WhatIf</span></span>
<span data-ttu-id="d9fb5-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d9fb5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9fb5-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9fb5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9fb5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9fb5-135">CommonParameters</span></span>
<span data-ttu-id="d9fb5-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9fb5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9fb5-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9fb5-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9fb5-138">입력</span><span class="sxs-lookup"><span data-stu-id="d9fb5-138">INPUTS</span></span>

### <span data-ttu-id="d9fb5-139">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d9fb5-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d9fb5-140">ApiManagement. ServiceManagement. \ PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="d9fb5-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>
<span data-ttu-id="d9fb5-141">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d9fb5-141">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="d9fb5-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d9fb5-142">System.String</span></span>

## <span data-ttu-id="d9fb5-143">출력</span><span class="sxs-lookup"><span data-stu-id="d9fb5-143">OUTPUTS</span></span>

### <span data-ttu-id="d9fb5-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="d9fb5-144">System.Boolean</span></span>

## <span data-ttu-id="d9fb5-145">상속자</span><span class="sxs-lookup"><span data-stu-id="d9fb5-145">NOTES</span></span>

## <span data-ttu-id="d9fb5-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d9fb5-146">RELATED LINKS</span></span>

[<span data-ttu-id="d9fb5-147">Get-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="d9fb5-147">Get-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="d9fb5-148">새로운 AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="d9fb5-148">New-AzureRmApiManagementApiRelease</span></span>](./New-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="d9fb5-149">Set-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="d9fb5-149">Set-AzureRmApiManagementApiRelease</span></span>](./Set-AzureRmApiManagementApiRelease.md)
