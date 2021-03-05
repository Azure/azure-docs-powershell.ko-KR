---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: ada7faf13457f2c074a15b6e409e31afb93ac900
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993547"
---
# <span data-ttu-id="6b860-101">Remove-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="6b860-101">Remove-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="6b860-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b860-102">SYNOPSIS</span></span>
<span data-ttu-id="6b860-103">DNS 영역 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6b860-103">Removes a DNS zone group.</span></span>

## <span data-ttu-id="6b860-104">구문</span><span class="sxs-lookup"><span data-stu-id="6b860-104">SYNTAX</span></span>

```
Remove-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b860-105">설명</span><span class="sxs-lookup"><span data-stu-id="6b860-105">DESCRIPTION</span></span>
<span data-ttu-id="6b860-106">**Remove-AzPrivateDnsZoneGroup** cmdlet은 DNS 영역 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6b860-106">The **Remove-AzPrivateDnsZoneGroup** cmdlet removes a DNS zone group.</span></span> 

## <span data-ttu-id="6b860-107">예제</span><span class="sxs-lookup"><span data-stu-id="6b860-107">EXAMPLES</span></span>

### <span data-ttu-id="6b860-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6b860-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name dnsgroup1 
```

<span data-ttu-id="6b860-109">위의 예제에서는 엔드포인트 테스트-pr-엔드포인트에서 dnsgroup1이라는 DNS 영역 grup을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6b860-109">Above example removes a DNS zone grup named dnsgroup1 from endpoint test-pr-endpoint.</span></span>

## <span data-ttu-id="6b860-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6b860-110">PARAMETERS</span></span>

### <span data-ttu-id="6b860-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b860-111">-AsJob</span></span>
<span data-ttu-id="6b860-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6b860-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b860-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b860-113">-DefaultProfile</span></span>
<span data-ttu-id="6b860-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6b860-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b860-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6b860-115">-Force</span></span>
<span data-ttu-id="6b860-116">리소스를 삭제하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b860-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="6b860-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6b860-117">-Name</span></span>
<span data-ttu-id="6b860-118">개인 dns 영역 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b860-118">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b860-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b860-119">-PassThru</span></span>
<span data-ttu-id="6b860-120">{{ Fill PassThru 설명 }}</span><span class="sxs-lookup"><span data-stu-id="6b860-120">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="6b860-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="6b860-121">-PrivateEndpointName</span></span>
<span data-ttu-id="6b860-122">개인 엔드포인트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b860-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="6b860-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b860-123">-ResourceGroupName</span></span>
<span data-ttu-id="6b860-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b860-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="6b860-125">-확인</span><span class="sxs-lookup"><span data-stu-id="6b860-125">-Confirm</span></span>
<span data-ttu-id="6b860-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b860-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b860-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b860-127">-WhatIf</span></span>
<span data-ttu-id="6b860-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6b860-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b860-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b860-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b860-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b860-130">CommonParameters</span></span>
<span data-ttu-id="6b860-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6b860-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b860-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b860-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b860-133">입력</span><span class="sxs-lookup"><span data-stu-id="6b860-133">INPUTS</span></span>

### <span data-ttu-id="6b860-134">System.String</span><span class="sxs-lookup"><span data-stu-id="6b860-134">System.String</span></span>

## <span data-ttu-id="6b860-135">출력</span><span class="sxs-lookup"><span data-stu-id="6b860-135">OUTPUTS</span></span>

### <span data-ttu-id="6b860-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6b860-136">System.Boolean</span></span>

## <span data-ttu-id="6b860-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6b860-137">NOTES</span></span>

## <span data-ttu-id="6b860-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6b860-138">RELATED LINKS</span></span>
