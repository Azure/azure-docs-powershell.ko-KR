---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: cd32f29a0202fa8c38abed43075a8623efe068a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524723"
---
# <span data-ttu-id="fd324-101">Remove-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="fd324-101">Remove-AzureRmApiManagementApiRevision</span></span>

## <span data-ttu-id="fd324-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd324-102">SYNOPSIS</span></span>
<span data-ttu-id="fd324-103">특정 API 개정판을 제거 했습니다.</span><span class="sxs-lookup"><span data-stu-id="fd324-103">Removed a particular API Revision</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd324-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fd324-104">SYNTAX</span></span>

### <span data-ttu-id="fd324-105">ByApiId (기본값)</span><span class="sxs-lookup"><span data-stu-id="fd324-105">ByApiId (Default)</span></span>
```
Remove-AzureRmApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd324-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fd324-106">ByInputObject</span></span>
```
Remove-AzureRmApiManagementApiRevision -InputObject <PsApiManagementApi> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd324-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fd324-107">DESCRIPTION</span></span>
<span data-ttu-id="fd324-108">Cmdlet **AzureRmApiManagementApiRevision** 는 특정 API 수정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd324-108">The cmdlet **Remove-AzureRmApiManagementApiRevision** removes a particular API revision.</span></span>

## <span data-ttu-id="fd324-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fd324-109">EXAMPLES</span></span>

### <span data-ttu-id="fd324-110">예제 1: API 수정 버전 제거</span><span class="sxs-lookup"><span data-stu-id="fd324-110">Example 1: Remove an API Revision</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiRevision -Context $apimContext -ApiId "echo-api" -ApiRevision "2"
```

<span data-ttu-id="fd324-111">이 명령은 `2` `echo-api` api Management 서비스에서 api의 수정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd324-111">This command removes the `2` revision of the API `echo-api` from API Management service.</span></span>

## <span data-ttu-id="fd324-112">변수</span><span class="sxs-lookup"><span data-stu-id="fd324-112">PARAMETERS</span></span>

### <span data-ttu-id="fd324-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="fd324-113">-ApiId</span></span>
<span data-ttu-id="fd324-114">API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="fd324-114">Identifier of the API.</span></span>
<span data-ttu-id="fd324-115">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="fd324-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd324-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="fd324-116">-ApiRevision</span></span>
<span data-ttu-id="fd324-117">API 개정판의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="fd324-117">Identifier of the API Revision.</span></span> <span data-ttu-id="fd324-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="fd324-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd324-119">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="fd324-119">-Context</span></span>
<span data-ttu-id="fd324-120">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="fd324-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="fd324-121">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="fd324-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd324-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd324-122">-DefaultProfile</span></span>
<span data-ttu-id="fd324-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fd324-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd324-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd324-124">-InputObject</span></span>
<span data-ttu-id="fd324-125">PsApiManagementApiRelease의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="fd324-125">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="fd324-126">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="fd324-126">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd324-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd324-127">-PassThru</span></span>
<span data-ttu-id="fd324-128">지정 된 경우 대/소문자 구분 작업이 성공한 경우 true를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="fd324-128">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="fd324-129">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="fd324-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="fd324-130">-확인</span><span class="sxs-lookup"><span data-stu-id="fd324-130">-Confirm</span></span>
<span data-ttu-id="fd324-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd324-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd324-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd324-132">-WhatIf</span></span>
<span data-ttu-id="fd324-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fd324-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd324-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd324-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd324-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd324-135">CommonParameters</span></span>
<span data-ttu-id="fd324-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd324-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd324-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd324-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd324-138">입력</span><span class="sxs-lookup"><span data-stu-id="fd324-138">INPUTS</span></span>

### <span data-ttu-id="fd324-139">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fd324-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fd324-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fd324-140">System.String</span></span>

### <span data-ttu-id="fd324-141">ApiManagement. ServiceManagement. \ PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fd324-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="fd324-142">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fd324-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="fd324-143">출력</span><span class="sxs-lookup"><span data-stu-id="fd324-143">OUTPUTS</span></span>

### <span data-ttu-id="fd324-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="fd324-144">System.Boolean</span></span>

## <span data-ttu-id="fd324-145">상속자</span><span class="sxs-lookup"><span data-stu-id="fd324-145">NOTES</span></span>

## <span data-ttu-id="fd324-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd324-146">RELATED LINKS</span></span>

[<span data-ttu-id="fd324-147">Get-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="fd324-147">Get-AzureRmApiManagementApiRevision</span></span>](./Get-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="fd324-148">새로운 AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="fd324-148">New-AzureRmApiManagementApiRevision</span></span>](./New-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="fd324-149">Set-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="fd324-149">Set-AzureRmApiManagementApiRevision</span></span>](./Set-AzureRmApiManagementApiRevision.md)
