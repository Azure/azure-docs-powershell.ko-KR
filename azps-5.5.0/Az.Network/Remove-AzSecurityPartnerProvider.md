---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
ms.openlocfilehash: a51345653580261178191687f54bf0f2a8cc6f0c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202516"
---
# <span data-ttu-id="cf002-101">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="cf002-101">Remove-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="cf002-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf002-102">SYNOPSIS</span></span>
<span data-ttu-id="cf002-103">Azure SecurityPartnerProvider를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="cf002-103">Deletes an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="cf002-104">구문</span><span class="sxs-lookup"><span data-stu-id="cf002-104">SYNTAX</span></span>

### <span data-ttu-id="cf002-105">SecurityPartnerProviderNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf002-105">SecurityPartnerProviderNameParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf002-106">SecurityPartnerProviderInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf002-106">SecurityPartnerProviderInputObjectParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf002-107">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf002-107">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf002-108">설명</span><span class="sxs-lookup"><span data-stu-id="cf002-108">DESCRIPTION</span></span>
<span data-ttu-id="cf002-109">**Remove-AzSecurityPartnerProvider** cmdlet은 Azure SecurityPartnerProvider를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="cf002-109">The **Remove-AzSecurityPartnerProvider** cmdlet deletes an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="cf002-110">예제</span><span class="sxs-lookup"><span data-stu-id="cf002-110">EXAMPLES</span></span>

### <span data-ttu-id="cf002-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="cf002-111">Example 1</span></span>
```powershell
Remove-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```

## <span data-ttu-id="cf002-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf002-112">PARAMETERS</span></span>

### <span data-ttu-id="cf002-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf002-113">-AsJob</span></span>
<span data-ttu-id="cf002-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="cf002-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cf002-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf002-115">-DefaultProfile</span></span>
<span data-ttu-id="cf002-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cf002-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf002-117">-Force</span><span class="sxs-lookup"><span data-stu-id="cf002-117">-Force</span></span>
<span data-ttu-id="cf002-118">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cf002-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cf002-119">-Name</span><span class="sxs-lookup"><span data-stu-id="cf002-119">-Name</span></span>
<span data-ttu-id="cf002-120">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf002-120">The resource name.</span></span>

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

### <span data-ttu-id="cf002-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf002-121">-PassThru</span></span>
<span data-ttu-id="cf002-122">이 작업이 수행되는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="cf002-122">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="cf002-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf002-123">-ResourceGroupName</span></span>
<span data-ttu-id="cf002-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf002-124">The resource group name.</span></span>

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

### <span data-ttu-id="cf002-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf002-125">-ResourceId</span></span>
<span data-ttu-id="cf002-126">securityPartnerProvider 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cf002-126">The securityPartnerProvider resource Id.</span></span>

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

### <span data-ttu-id="cf002-127">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="cf002-127">-SecurityPartnerProvider</span></span>
<span data-ttu-id="cf002-128">securityPartnerProvider 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="cf002-128">The securityPartnerProvider input object.</span></span>

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

### <span data-ttu-id="cf002-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf002-129">-Confirm</span></span>
<span data-ttu-id="cf002-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf002-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf002-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf002-131">-WhatIf</span></span>
<span data-ttu-id="cf002-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="cf002-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf002-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cf002-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf002-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf002-134">CommonParameters</span></span>
<span data-ttu-id="cf002-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cf002-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf002-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cf002-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf002-137">입력</span><span class="sxs-lookup"><span data-stu-id="cf002-137">INPUTS</span></span>

### <span data-ttu-id="cf002-138">System.String</span><span class="sxs-lookup"><span data-stu-id="cf002-138">System.String</span></span>

### <span data-ttu-id="cf002-139">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="cf002-139">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="cf002-140">출력</span><span class="sxs-lookup"><span data-stu-id="cf002-140">OUTPUTS</span></span>

### <span data-ttu-id="cf002-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cf002-141">System.Boolean</span></span>

## <span data-ttu-id="cf002-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cf002-142">NOTES</span></span>

## <span data-ttu-id="cf002-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cf002-143">RELATED LINKS</span></span>
