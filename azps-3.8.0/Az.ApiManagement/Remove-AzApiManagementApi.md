---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
ms.openlocfilehash: 13f5297efc19aa56cc5af55962c072f5ff2a32d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042197"
---
# <span data-ttu-id="dbcd0-101">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dbcd0-101">Remove-AzApiManagementApi</span></span>

## <span data-ttu-id="dbcd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbcd0-102">SYNOPSIS</span></span>
<span data-ttu-id="dbcd0-103">API를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-103">Removes an API.</span></span>

## <span data-ttu-id="dbcd0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dbcd0-104">SYNTAX</span></span>

```
Remove-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbcd0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dbcd0-105">DESCRIPTION</span></span>
<span data-ttu-id="dbcd0-106">**Remove-AzApiManagementApi** cmdlet은 기존 API를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-106">The **Remove-AzApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="dbcd0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dbcd0-107">EXAMPLES</span></span>

### <span data-ttu-id="dbcd0-108">예제 1: API 제거</span><span class="sxs-lookup"><span data-stu-id="dbcd0-108">Example 1: Remove an API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="dbcd0-109">이 명령은 지정 된 ID의 API를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="dbcd0-110">변수</span><span class="sxs-lookup"><span data-stu-id="dbcd0-110">PARAMETERS</span></span>

### <span data-ttu-id="dbcd0-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="dbcd0-111">-ApiId</span></span>
<span data-ttu-id="dbcd0-112">API 제거의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="dbcd0-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="dbcd0-113">-Context</span></span>
<span data-ttu-id="dbcd0-114">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbcd0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbcd0-115">-DefaultProfile</span></span>
<span data-ttu-id="dbcd0-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbcd0-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dbcd0-117">-PassThru</span></span>
<span data-ttu-id="dbcd0-118">passthru</span><span class="sxs-lookup"><span data-stu-id="dbcd0-118">passthru</span></span>

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

### <span data-ttu-id="dbcd0-119">-확인</span><span class="sxs-lookup"><span data-stu-id="dbcd0-119">-Confirm</span></span>
<span data-ttu-id="dbcd0-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbcd0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbcd0-121">-WhatIf</span></span>
<span data-ttu-id="dbcd0-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbcd0-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbcd0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbcd0-124">CommonParameters</span></span>
<span data-ttu-id="dbcd0-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbcd0-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbcd0-127">입력</span><span class="sxs-lookup"><span data-stu-id="dbcd0-127">INPUTS</span></span>

### <span data-ttu-id="dbcd0-128">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dbcd0-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dbcd0-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dbcd0-129">System.String</span></span>

### <span data-ttu-id="dbcd0-130">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="dbcd0-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dbcd0-131">출력</span><span class="sxs-lookup"><span data-stu-id="dbcd0-131">OUTPUTS</span></span>

### <span data-ttu-id="dbcd0-132">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="dbcd0-132">System.Boolean</span></span>

## <span data-ttu-id="dbcd0-133">상속자</span><span class="sxs-lookup"><span data-stu-id="dbcd0-133">NOTES</span></span>

## <span data-ttu-id="dbcd0-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dbcd0-134">RELATED LINKS</span></span>

[<span data-ttu-id="dbcd0-135">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dbcd0-135">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="dbcd0-136">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dbcd0-136">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="dbcd0-137">가져오기-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dbcd0-137">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="dbcd0-138">새로운 AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dbcd0-138">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="dbcd0-139">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dbcd0-139">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


