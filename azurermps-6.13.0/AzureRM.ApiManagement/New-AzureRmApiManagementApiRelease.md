---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: cb7fbfe4ba4fdf09b9012ddc5be8028af0bd80c1
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93538276"
---
# <span data-ttu-id="68a29-101">New-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="68a29-101">New-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="68a29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68a29-102">SYNOPSIS</span></span>
<span data-ttu-id="68a29-103">API 개정판의 API 릴리스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="68a29-103">Creates an API Release of an API Revision</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68a29-104">구문과</span><span class="sxs-lookup"><span data-stu-id="68a29-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="68a29-105">설명은</span><span class="sxs-lookup"><span data-stu-id="68a29-105">DESCRIPTION</span></span>

<span data-ttu-id="68a29-106">**AzureRmApiManagementApiRelease** cmdlet은 api MANAGEMENT 컨텍스트에서 api 개정판에 대 한 api 릴리스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="68a29-106">The **New-AzureRmApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span>

## <span data-ttu-id="68a29-107">예제의</span><span class="sxs-lookup"><span data-stu-id="68a29-107">EXAMPLES</span></span>

### <span data-ttu-id="68a29-108">예제 1: API 수정에 대 한 API 릴리스 만들기</span><span class="sxs-lookup"><span data-stu-id="68a29-108">Example 1: Create an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementApiRelease -Context $context  -ApiId 5adf6fbf0faadf3ad8558065 -ApiRevision 6 -Note "Releasing version 6"


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

<span data-ttu-id="68a29-109">이 명령은의 버전에 대 한 API 릴리스를 만듭니다 `2` `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="68a29-109">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="68a29-110">변수</span><span class="sxs-lookup"><span data-stu-id="68a29-110">PARAMETERS</span></span>

### <span data-ttu-id="68a29-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="68a29-111">-ApiId</span></span>
<span data-ttu-id="68a29-112">새 API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="68a29-112">Identifier for new API.</span></span>

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

### <span data-ttu-id="68a29-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="68a29-113">-ApiRevision</span></span>
<span data-ttu-id="68a29-114">Api 개정판에 대 한 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="68a29-114">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="68a29-115">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="68a29-115">-Context</span></span>
<span data-ttu-id="68a29-116">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="68a29-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="68a29-117">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="68a29-117">This parameter is required.</span></span>

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

### <span data-ttu-id="68a29-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68a29-118">-DefaultProfile</span></span>
<span data-ttu-id="68a29-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68a29-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68a29-120">-메모</span><span class="sxs-lookup"><span data-stu-id="68a29-120">-Note</span></span>
<span data-ttu-id="68a29-121">Api 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="68a29-121">Api Release Notes.</span></span> <span data-ttu-id="68a29-122">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="68a29-122">This parameter is optional</span></span>

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

### <span data-ttu-id="68a29-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="68a29-123">-ReleaseId</span></span>
<span data-ttu-id="68a29-124">Api 릴리스의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="68a29-124">Identifier for the Api Release.</span></span>
<span data-ttu-id="68a29-125">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="68a29-125">This parameter is optional.</span></span>
<span data-ttu-id="68a29-126">지정 하지 않으면 식별자가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="68a29-126">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="68a29-127">-확인</span><span class="sxs-lookup"><span data-stu-id="68a29-127">-Confirm</span></span>
<span data-ttu-id="68a29-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a29-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68a29-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68a29-129">-WhatIf</span></span>
<span data-ttu-id="68a29-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="68a29-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68a29-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68a29-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68a29-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68a29-132">CommonParameters</span></span>
<span data-ttu-id="68a29-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a29-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68a29-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68a29-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68a29-135">입력</span><span class="sxs-lookup"><span data-stu-id="68a29-135">INPUTS</span></span>

### <span data-ttu-id="68a29-136">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="68a29-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="68a29-137">매개 변수: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="68a29-137">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="68a29-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="68a29-138">System.String</span></span>

## <span data-ttu-id="68a29-139">출력</span><span class="sxs-lookup"><span data-stu-id="68a29-139">OUTPUTS</span></span>

### <span data-ttu-id="68a29-140">ApiManagement. ServiceManagement. \ PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="68a29-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="68a29-141">상속자</span><span class="sxs-lookup"><span data-stu-id="68a29-141">NOTES</span></span>

## <span data-ttu-id="68a29-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68a29-142">RELATED LINKS</span></span>

[<span data-ttu-id="68a29-143">Get-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="68a29-143">Get-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="68a29-144">제거-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="68a29-144">Remove-AzureRmApiManagementApiRelease</span></span>](./Remove-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="68a29-145">Set-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="68a29-145">Set-AzureRmApiManagementApiRelease</span></span>](./Set-AzureRmApiManagementApiRelease.md)
