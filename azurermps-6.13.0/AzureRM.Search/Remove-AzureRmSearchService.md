---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/remove-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Remove-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Remove-AzureRmSearchService.md
ms.openlocfilehash: c558a5d7228253e0a76b0d47fb21f581b4e06f11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532351"
---
# <span data-ttu-id="4b2f7-101">Remove-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="4b2f7-101">Remove-AzureRmSearchService</span></span>

## <span data-ttu-id="4b2f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b2f7-102">SYNOPSIS</span></span>
<span data-ttu-id="4b2f7-103">Azure Search service를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b2f7-103">Remove an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b2f7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4b2f7-104">SYNTAX</span></span>

### <span data-ttu-id="4b2f7-105">ResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="4b2f7-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzureRmSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b2f7-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b2f7-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b2f7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b2f7-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmSearchService [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b2f7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4b2f7-108">DESCRIPTION</span></span>
<span data-ttu-id="4b2f7-109">**AzureRmSearchService** cmdlet은 지정 된 Paramters Azure Search 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b2f7-109">The **Remove-AzureRmSearchService** cmdlet removes an Azure Search service with specified paramters.</span></span>

## <span data-ttu-id="4b2f7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4b2f7-110">EXAMPLES</span></span>

### <span data-ttu-id="4b2f7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4b2f7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="4b2f7-112">이 예제에서는 Azure Search 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b2f7-112">The example removes an Azure Search service.</span></span>

## <span data-ttu-id="4b2f7-113">변수</span><span class="sxs-lookup"><span data-stu-id="4b2f7-113">PARAMETERS</span></span>

### <span data-ttu-id="4b2f7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b2f7-114">-DefaultProfile</span></span>
<span data-ttu-id="4b2f7-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4b2f7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b2f7-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4b2f7-116">-Force</span></span>
<span data-ttu-id="4b2f7-117">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4b2f7-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4b2f7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b2f7-118">-InputObject</span></span>
<span data-ttu-id="4b2f7-119">검색 서비스 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4b2f7-119">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b2f7-120">-이름</span><span class="sxs-lookup"><span data-stu-id="4b2f7-120">-Name</span></span>
<span data-ttu-id="4b2f7-121">검색 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b2f7-121">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b2f7-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b2f7-122">-PassThru</span></span>
<span data-ttu-id="4b2f7-123">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4b2f7-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="4b2f7-124">이 스위치를 지정 하면 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b2f7-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="4b2f7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b2f7-125">-ResourceGroupName</span></span>
<span data-ttu-id="4b2f7-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b2f7-126">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b2f7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b2f7-127">-ResourceId</span></span>
<span data-ttu-id="4b2f7-128">검색 서비스 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="4b2f7-128">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b2f7-129">-확인</span><span class="sxs-lookup"><span data-stu-id="4b2f7-129">-Confirm</span></span>
<span data-ttu-id="4b2f7-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b2f7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b2f7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b2f7-131">-WhatIf</span></span>
<span data-ttu-id="4b2f7-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4b2f7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b2f7-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4b2f7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b2f7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b2f7-134">CommonParameters</span></span>
<span data-ttu-id="4b2f7-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b2f7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b2f7-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b2f7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b2f7-137">입력</span><span class="sxs-lookup"><span data-stu-id="4b2f7-137">INPUTS</span></span>

### <span data-ttu-id="4b2f7-138">Microsoft. Azure. PSSearchService를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b2f7-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="4b2f7-139">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4b2f7-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="4b2f7-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4b2f7-140">System.String</span></span>

## <span data-ttu-id="4b2f7-141">출력</span><span class="sxs-lookup"><span data-stu-id="4b2f7-141">OUTPUTS</span></span>

### <span data-ttu-id="4b2f7-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="4b2f7-142">System.Boolean</span></span>

## <span data-ttu-id="4b2f7-143">상속자</span><span class="sxs-lookup"><span data-stu-id="4b2f7-143">NOTES</span></span>

## <span data-ttu-id="4b2f7-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b2f7-144">RELATED LINKS</span></span>

[<span data-ttu-id="4b2f7-145">새로운 AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="4b2f7-145">New-AzureRmSearchService</span></span>](./New-AzureRmSearchService.md)

[<span data-ttu-id="4b2f7-146">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="4b2f7-146">Get-AzureRmSearchService</span></span>](./Get-AzureRmSearchService.md)

[<span data-ttu-id="4b2f7-147">Set-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="4b2f7-147">Set-AzureRmSearchService</span></span>](./Set-AzureRmSearchService.md)

