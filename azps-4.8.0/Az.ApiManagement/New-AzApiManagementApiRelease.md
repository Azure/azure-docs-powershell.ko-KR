---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: 263e54adc39103a704dc4ea0bd30f396b5d00fc9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94049242"
---
# <span data-ttu-id="e5fee-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="e5fee-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="e5fee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5fee-102">SYNOPSIS</span></span>
<span data-ttu-id="e5fee-103">API 개정판의 API 릴리스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5fee-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="e5fee-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e5fee-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5fee-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e5fee-105">DESCRIPTION</span></span>

<span data-ttu-id="e5fee-106">**AzApiManagementApiRelease** cmdlet은 api MANAGEMENT 컨텍스트에서 api 개정판에 대 한 api 릴리스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5fee-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span> <span data-ttu-id="e5fee-107">릴리스는 Api 수정을 현재 수정 버전으로 만드는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5fee-107">A Release is used to make the Api Revision as Current Revision.</span></span>

## <span data-ttu-id="e5fee-108">예제의</span><span class="sxs-lookup"><span data-stu-id="e5fee-108">EXAMPLES</span></span>

### <span data-ttu-id="e5fee-109">예제 1: API 수정에 대 한 API 릴리스 만들기</span><span class="sxs-lookup"><span data-stu-id="e5fee-109">Example 1: Create an API Release for an API Revision</span></span>
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

<span data-ttu-id="e5fee-110">이 명령은의 버전에 대 한 API 릴리스를 만듭니다 `2` `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="e5fee-110">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="e5fee-111">변수</span><span class="sxs-lookup"><span data-stu-id="e5fee-111">PARAMETERS</span></span>

### <span data-ttu-id="e5fee-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e5fee-112">-ApiId</span></span>
<span data-ttu-id="e5fee-113">새 API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e5fee-113">Identifier for new API.</span></span>

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

### <span data-ttu-id="e5fee-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="e5fee-114">-ApiRevision</span></span>
<span data-ttu-id="e5fee-115">Api 개정판에 대 한 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e5fee-115">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="e5fee-116">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="e5fee-116">-Context</span></span>
<span data-ttu-id="e5fee-117">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="e5fee-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e5fee-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="e5fee-118">This parameter is required.</span></span>

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

### <span data-ttu-id="e5fee-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5fee-119">-DefaultProfile</span></span>
<span data-ttu-id="e5fee-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e5fee-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5fee-121">-메모</span><span class="sxs-lookup"><span data-stu-id="e5fee-121">-Note</span></span>
<span data-ttu-id="e5fee-122">Api 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="e5fee-122">Api Release Notes.</span></span> <span data-ttu-id="e5fee-123">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="e5fee-123">This parameter is optional</span></span>

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

### <span data-ttu-id="e5fee-124">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="e5fee-124">-ReleaseId</span></span>
<span data-ttu-id="e5fee-125">Api 릴리스의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e5fee-125">Identifier for the Api Release.</span></span>
<span data-ttu-id="e5fee-126">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="e5fee-126">This parameter is optional.</span></span>
<span data-ttu-id="e5fee-127">지정 하지 않으면 식별자가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5fee-127">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="e5fee-128">-확인</span><span class="sxs-lookup"><span data-stu-id="e5fee-128">-Confirm</span></span>
<span data-ttu-id="e5fee-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5fee-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5fee-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5fee-130">-WhatIf</span></span>
<span data-ttu-id="e5fee-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e5fee-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5fee-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e5fee-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5fee-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5fee-133">CommonParameters</span></span>
<span data-ttu-id="e5fee-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5fee-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5fee-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e5fee-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5fee-136">입력</span><span class="sxs-lookup"><span data-stu-id="e5fee-136">INPUTS</span></span>

### <span data-ttu-id="e5fee-137">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e5fee-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e5fee-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e5fee-138">System.String</span></span>

## <span data-ttu-id="e5fee-139">출력</span><span class="sxs-lookup"><span data-stu-id="e5fee-139">OUTPUTS</span></span>

### <span data-ttu-id="e5fee-140">ApiManagement. ServiceManagement. \ PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="e5fee-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="e5fee-141">상속자</span><span class="sxs-lookup"><span data-stu-id="e5fee-141">NOTES</span></span>

## <span data-ttu-id="e5fee-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e5fee-142">RELATED LINKS</span></span>

[<span data-ttu-id="e5fee-143">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="e5fee-143">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="e5fee-144">제거-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="e5fee-144">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="e5fee-145">업데이트-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="e5fee-145">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)