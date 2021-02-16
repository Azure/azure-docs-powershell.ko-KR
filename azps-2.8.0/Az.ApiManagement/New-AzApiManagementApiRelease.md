---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: 5a5d155b8c9127d330a1f53d1fe53d42d60d46a8
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406607"
---
# <span data-ttu-id="aa6b3-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="aa6b3-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="aa6b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa6b3-102">SYNOPSIS</span></span>
<span data-ttu-id="aa6b3-103">API 개정의 API 릴리스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aa6b3-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="aa6b3-104">구문</span><span class="sxs-lookup"><span data-stu-id="aa6b3-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aa6b3-105">설명</span><span class="sxs-lookup"><span data-stu-id="aa6b3-105">DESCRIPTION</span></span>

<span data-ttu-id="aa6b3-106">**New-AzApiManagementApiRelease** cmdlet은 API Management 컨텍스트에서 API 개정에 대한 API 릴리스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aa6b3-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span> <span data-ttu-id="aa6b3-107">릴리스는 Api 개정을 현재 버전으로 만드는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="aa6b3-107">A Release is used to make the Api Revision as Current Revision.</span></span>

## <span data-ttu-id="aa6b3-108">예제</span><span class="sxs-lookup"><span data-stu-id="aa6b3-108">EXAMPLES</span></span>

### <span data-ttu-id="aa6b3-109">예제 1: API 개정에 대한 API 릴리스 만들기</span><span class="sxs-lookup"><span data-stu-id="aa6b3-109">Example 1: Create an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRelease -Context $context  -ApiId 5adf6fbf0faadf3ad8558065 -ApiRevision 6 -Note "Releasing version 6"


ReleaseId         : 7e4d3fbb43c146c4bf406499ef9411f4
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 1:16:29 AM
UpdatedDateTime   : 5/17/2018 1:16:29 AM
Notes             : Releasing version 6
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/7e4d3fbb43c146c4bf40649
                    9ef9411f4
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="aa6b3-110">이 명령은 .의 버전에 대한 API `2` 릴리스를 `echo-api` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aa6b3-110">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="aa6b3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa6b3-111">PARAMETERS</span></span>

### <span data-ttu-id="aa6b3-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="aa6b3-112">-ApiId</span></span>
<span data-ttu-id="aa6b3-113">새 API에 대한 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="aa6b3-113">Identifier for new API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa6b3-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="aa6b3-114">-ApiRevision</span></span>
<span data-ttu-id="aa6b3-115">API 개정에 대한 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="aa6b3-115">Identifier for the Api Revision.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa6b3-116">-Context</span><span class="sxs-lookup"><span data-stu-id="aa6b3-116">-Context</span></span>
<span data-ttu-id="aa6b3-117">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="aa6b3-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="aa6b3-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="aa6b3-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa6b3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa6b3-119">-DefaultProfile</span></span>
<span data-ttu-id="aa6b3-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aa6b3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa6b3-121">-Note</span><span class="sxs-lookup"><span data-stu-id="aa6b3-121">-Note</span></span>
<span data-ttu-id="aa6b3-122">API 릴리스 정보.</span><span class="sxs-lookup"><span data-stu-id="aa6b3-122">Api Release Notes.</span></span> <span data-ttu-id="aa6b3-123">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="aa6b3-123">This parameter is optional</span></span>

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

### <span data-ttu-id="aa6b3-124">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="aa6b3-124">-ReleaseId</span></span>
<span data-ttu-id="aa6b3-125">API 릴리스의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="aa6b3-125">Identifier for the Api Release.</span></span>
<span data-ttu-id="aa6b3-126">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="aa6b3-126">This parameter is optional.</span></span>
<span data-ttu-id="aa6b3-127">지정하지 않으면 식별자가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="aa6b3-127">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="aa6b3-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa6b3-128">-Confirm</span></span>
<span data-ttu-id="aa6b3-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="aa6b3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa6b3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa6b3-130">-WhatIf</span></span>
<span data-ttu-id="aa6b3-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="aa6b3-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aa6b3-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aa6b3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa6b3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa6b3-133">CommonParameters</span></span>
<span data-ttu-id="aa6b3-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aa6b3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa6b3-135">자세한 내용은 [다음](https://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aa6b3-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa6b3-136">입력</span><span class="sxs-lookup"><span data-stu-id="aa6b3-136">INPUTS</span></span>

### <span data-ttu-id="aa6b3-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="aa6b3-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="aa6b3-138">System.String</span><span class="sxs-lookup"><span data-stu-id="aa6b3-138">System.String</span></span>

## <span data-ttu-id="aa6b3-139">출력</span><span class="sxs-lookup"><span data-stu-id="aa6b3-139">OUTPUTS</span></span>

### <span data-ttu-id="aa6b3-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="aa6b3-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="aa6b3-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aa6b3-141">NOTES</span></span>

## <span data-ttu-id="aa6b3-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aa6b3-142">RELATED LINKS</span></span>

[<span data-ttu-id="aa6b3-143">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="aa6b3-143">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="aa6b3-144">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="aa6b3-144">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="aa6b3-145">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="aa6b3-145">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)