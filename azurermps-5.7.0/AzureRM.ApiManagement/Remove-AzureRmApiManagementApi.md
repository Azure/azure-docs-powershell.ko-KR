---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
ms.openlocfilehash: 4bcda06e1c00e338feb80584fb6e2b51a63b051d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711458"
---
# <span data-ttu-id="7780a-101">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7780a-101">Remove-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="7780a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7780a-102">SYNOPSIS</span></span>
<span data-ttu-id="7780a-103">API를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7780a-103">Removes an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7780a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7780a-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7780a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7780a-105">DESCRIPTION</span></span>
<span data-ttu-id="7780a-106">**Remove-AzureRmApiManagementApi** cmdlet은 기존 API를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7780a-106">The **Remove-AzureRmApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="7780a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7780a-107">EXAMPLES</span></span>

### <span data-ttu-id="7780a-108">예제 1: API 제거</span><span class="sxs-lookup"><span data-stu-id="7780a-108">Example 1: Remove an API</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="7780a-109">이 명령은 지정 된 ID의 API를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7780a-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="7780a-110">변수</span><span class="sxs-lookup"><span data-stu-id="7780a-110">PARAMETERS</span></span>

### <span data-ttu-id="7780a-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="7780a-111">-ApiId</span></span>
<span data-ttu-id="7780a-112">API 제거의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7780a-112">Specifies the ID of the API remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7780a-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="7780a-113">-Context</span></span>
<span data-ttu-id="7780a-114">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7780a-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7780a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7780a-115">-DefaultProfile</span></span>
<span data-ttu-id="7780a-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7780a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7780a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7780a-117">-PassThru</span></span>
<span data-ttu-id="7780a-118">passthru</span><span class="sxs-lookup"><span data-stu-id="7780a-118">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7780a-119">-확인</span><span class="sxs-lookup"><span data-stu-id="7780a-119">-Confirm</span></span>
<span data-ttu-id="7780a-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7780a-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7780a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7780a-121">-WhatIf</span></span>
<span data-ttu-id="7780a-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7780a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7780a-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7780a-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7780a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7780a-124">CommonParameters</span></span>
<span data-ttu-id="7780a-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7780a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7780a-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7780a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7780a-127">입력</span><span class="sxs-lookup"><span data-stu-id="7780a-127">INPUTS</span></span>

### <span data-ttu-id="7780a-128">않아야</span><span class="sxs-lookup"><span data-stu-id="7780a-128">None</span></span>
<span data-ttu-id="7780a-129">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7780a-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7780a-130">출력</span><span class="sxs-lookup"><span data-stu-id="7780a-130">OUTPUTS</span></span>

### <span data-ttu-id="7780a-131">나타내는</span><span class="sxs-lookup"><span data-stu-id="7780a-131">Boolean</span></span>

## <span data-ttu-id="7780a-132">상속자</span><span class="sxs-lookup"><span data-stu-id="7780a-132">NOTES</span></span>

## <span data-ttu-id="7780a-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7780a-133">RELATED LINKS</span></span>

[<span data-ttu-id="7780a-134">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7780a-134">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="7780a-135">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7780a-135">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="7780a-136">가져오기-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7780a-136">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="7780a-137">새로운 AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7780a-137">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="7780a-138">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7780a-138">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


