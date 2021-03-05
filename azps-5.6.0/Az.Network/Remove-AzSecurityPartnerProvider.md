---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
ms.openlocfilehash: 3fda360369615c28647769e6bc5aeb0af71e0e35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006171"
---
# <span data-ttu-id="54e84-101">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="54e84-101">Remove-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="54e84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54e84-102">SYNOPSIS</span></span>
<span data-ttu-id="54e84-103">Azure SecurityPartnerProvider를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="54e84-103">Deletes an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="54e84-104">구문</span><span class="sxs-lookup"><span data-stu-id="54e84-104">SYNTAX</span></span>

### <span data-ttu-id="54e84-105">SecurityPartnerProviderNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="54e84-105">SecurityPartnerProviderNameParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54e84-106">SecurityPartnerProviderInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54e84-106">SecurityPartnerProviderInputObjectParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54e84-107">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="54e84-107">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54e84-108">설명</span><span class="sxs-lookup"><span data-stu-id="54e84-108">DESCRIPTION</span></span>
<span data-ttu-id="54e84-109">**Remove-AzSecurityPartnerProvider** cmdlet은 Azure SecurityPartnerProvider를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="54e84-109">The **Remove-AzSecurityPartnerProvider** cmdlet deletes an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="54e84-110">예제</span><span class="sxs-lookup"><span data-stu-id="54e84-110">EXAMPLES</span></span>

### <span data-ttu-id="54e84-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="54e84-111">Example 1</span></span>
```powershell
Remove-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```

## <span data-ttu-id="54e84-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="54e84-112">PARAMETERS</span></span>

### <span data-ttu-id="54e84-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54e84-113">-AsJob</span></span>
<span data-ttu-id="54e84-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="54e84-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54e84-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54e84-115">-DefaultProfile</span></span>
<span data-ttu-id="54e84-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="54e84-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54e84-117">-Force</span><span class="sxs-lookup"><span data-stu-id="54e84-117">-Force</span></span>
<span data-ttu-id="54e84-118">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="54e84-118">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54e84-119">-Name</span><span class="sxs-lookup"><span data-stu-id="54e84-119">-Name</span></span>
<span data-ttu-id="54e84-120">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="54e84-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54e84-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54e84-121">-PassThru</span></span>
<span data-ttu-id="54e84-122">이 작업이 수행되는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="54e84-122">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54e84-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54e84-123">-ResourceGroupName</span></span>
<span data-ttu-id="54e84-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="54e84-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54e84-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54e84-125">-ResourceId</span></span>
<span data-ttu-id="54e84-126">securityPartnerProvider 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="54e84-126">The securityPartnerProvider resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54e84-127">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="54e84-127">-SecurityPartnerProvider</span></span>
<span data-ttu-id="54e84-128">securityPartnerProvider 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="54e84-128">The securityPartnerProvider input object.</span></span>

```yaml
Type: PSSecurityPartnerProvider
Parameter Sets: SecurityPartnerProviderInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54e84-129">-확인</span><span class="sxs-lookup"><span data-stu-id="54e84-129">-Confirm</span></span>
<span data-ttu-id="54e84-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="54e84-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54e84-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54e84-131">-WhatIf</span></span>
<span data-ttu-id="54e84-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="54e84-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54e84-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="54e84-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54e84-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54e84-134">CommonParameters</span></span>
<span data-ttu-id="54e84-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="54e84-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54e84-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54e84-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54e84-137">입력</span><span class="sxs-lookup"><span data-stu-id="54e84-137">INPUTS</span></span>

### <span data-ttu-id="54e84-138">System.String</span><span class="sxs-lookup"><span data-stu-id="54e84-138">System.String</span></span>

### <span data-ttu-id="54e84-139">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="54e84-139">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="54e84-140">출력</span><span class="sxs-lookup"><span data-stu-id="54e84-140">OUTPUTS</span></span>

### <span data-ttu-id="54e84-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="54e84-141">System.Boolean</span></span>

## <span data-ttu-id="54e84-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="54e84-142">NOTES</span></span>

## <span data-ttu-id="54e84-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="54e84-143">RELATED LINKS</span></span>
