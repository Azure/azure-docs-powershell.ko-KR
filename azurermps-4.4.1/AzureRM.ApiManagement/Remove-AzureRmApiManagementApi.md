---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
ms.openlocfilehash: cadae96af05ae11f76d3a8ea0010da4d73161186
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525791"
---
# <span data-ttu-id="41c16-101">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="41c16-101">Remove-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="41c16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41c16-102">SYNOPSIS</span></span>
<span data-ttu-id="41c16-103">API를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="41c16-103">Removes an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41c16-104">구문과</span><span class="sxs-lookup"><span data-stu-id="41c16-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41c16-105">설명은</span><span class="sxs-lookup"><span data-stu-id="41c16-105">DESCRIPTION</span></span>
<span data-ttu-id="41c16-106">**Remove-AzureRmApiManagementApi** cmdlet은 기존 API를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="41c16-106">The **Remove-AzureRmApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="41c16-107">예제의</span><span class="sxs-lookup"><span data-stu-id="41c16-107">EXAMPLES</span></span>

### <span data-ttu-id="41c16-108">예제 1: API 제거</span><span class="sxs-lookup"><span data-stu-id="41c16-108">Example 1: Remove an API</span></span>
```
PS C:\>Remove-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789"
```

<span data-ttu-id="41c16-109">이 명령은 지정 된 ID의 API를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="41c16-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="41c16-110">변수</span><span class="sxs-lookup"><span data-stu-id="41c16-110">PARAMETERS</span></span>

### <span data-ttu-id="41c16-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="41c16-111">-ApiId</span></span>
<span data-ttu-id="41c16-112">API 제거의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41c16-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="41c16-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="41c16-113">-Context</span></span>
<span data-ttu-id="41c16-114">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41c16-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41c16-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41c16-115">-PassThru</span></span>
<span data-ttu-id="41c16-116">passthru</span><span class="sxs-lookup"><span data-stu-id="41c16-116">passthru</span></span>

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

### <span data-ttu-id="41c16-117">-확인</span><span class="sxs-lookup"><span data-stu-id="41c16-117">-Confirm</span></span>
<span data-ttu-id="41c16-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="41c16-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41c16-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41c16-119">-WhatIf</span></span>
<span data-ttu-id="41c16-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="41c16-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41c16-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="41c16-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41c16-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41c16-122">-DefaultProfile</span></span>
<span data-ttu-id="41c16-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="41c16-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41c16-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41c16-124">CommonParameters</span></span>
<span data-ttu-id="41c16-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="41c16-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41c16-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41c16-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41c16-127">입력</span><span class="sxs-lookup"><span data-stu-id="41c16-127">INPUTS</span></span>

## <span data-ttu-id="41c16-128">출력</span><span class="sxs-lookup"><span data-stu-id="41c16-128">OUTPUTS</span></span>

### <span data-ttu-id="41c16-129">나타내는</span><span class="sxs-lookup"><span data-stu-id="41c16-129">Boolean</span></span>

## <span data-ttu-id="41c16-130">상속자</span><span class="sxs-lookup"><span data-stu-id="41c16-130">NOTES</span></span>

## <span data-ttu-id="41c16-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="41c16-131">RELATED LINKS</span></span>

[<span data-ttu-id="41c16-132">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="41c16-132">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="41c16-133">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="41c16-133">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="41c16-134">가져오기-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="41c16-134">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="41c16-135">새로운 AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="41c16-135">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="41c16-136">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="41c16-136">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


