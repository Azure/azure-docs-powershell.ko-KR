---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
ms.openlocfilehash: 3aedfc34d3f11abeea598e3ab5a891a3f4ee4526
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698006"
---
# <span data-ttu-id="14563-101">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="14563-101">Remove-AzApiManagementApi</span></span>

## <span data-ttu-id="14563-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14563-102">SYNOPSIS</span></span>
<span data-ttu-id="14563-103">API를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="14563-103">Removes an API.</span></span>

## <span data-ttu-id="14563-104">구문과</span><span class="sxs-lookup"><span data-stu-id="14563-104">SYNTAX</span></span>

```
Remove-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14563-105">설명은</span><span class="sxs-lookup"><span data-stu-id="14563-105">DESCRIPTION</span></span>
<span data-ttu-id="14563-106">**Remove-AzApiManagementApi** cmdlet은 기존 API를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="14563-106">The **Remove-AzApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="14563-107">예제의</span><span class="sxs-lookup"><span data-stu-id="14563-107">EXAMPLES</span></span>

### <span data-ttu-id="14563-108">예제 1: API 제거</span><span class="sxs-lookup"><span data-stu-id="14563-108">Example 1: Remove an API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="14563-109">이 명령은 지정 된 ID의 API를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="14563-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="14563-110">변수</span><span class="sxs-lookup"><span data-stu-id="14563-110">PARAMETERS</span></span>

### <span data-ttu-id="14563-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="14563-111">-ApiId</span></span>
<span data-ttu-id="14563-112">API 제거의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14563-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="14563-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="14563-113">-Context</span></span>
<span data-ttu-id="14563-114">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14563-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="14563-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14563-115">-DefaultProfile</span></span>
<span data-ttu-id="14563-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14563-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14563-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14563-117">-PassThru</span></span>
<span data-ttu-id="14563-118">passthru</span><span class="sxs-lookup"><span data-stu-id="14563-118">passthru</span></span>

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

### <span data-ttu-id="14563-119">-확인</span><span class="sxs-lookup"><span data-stu-id="14563-119">-Confirm</span></span>
<span data-ttu-id="14563-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="14563-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14563-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14563-121">-WhatIf</span></span>
<span data-ttu-id="14563-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="14563-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14563-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="14563-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14563-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14563-124">CommonParameters</span></span>
<span data-ttu-id="14563-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="14563-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14563-126">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="14563-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14563-127">입력</span><span class="sxs-lookup"><span data-stu-id="14563-127">INPUTS</span></span>

### <span data-ttu-id="14563-128">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="14563-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="14563-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="14563-129">System.String</span></span>

### <span data-ttu-id="14563-130">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="14563-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="14563-131">출력</span><span class="sxs-lookup"><span data-stu-id="14563-131">OUTPUTS</span></span>

### <span data-ttu-id="14563-132">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="14563-132">System.Boolean</span></span>

## <span data-ttu-id="14563-133">상속자</span><span class="sxs-lookup"><span data-stu-id="14563-133">NOTES</span></span>

## <span data-ttu-id="14563-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14563-134">RELATED LINKS</span></span>

[<span data-ttu-id="14563-135">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="14563-135">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="14563-136">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="14563-136">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="14563-137">가져오기-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="14563-137">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="14563-138">새로운 AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="14563-138">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="14563-139">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="14563-139">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


