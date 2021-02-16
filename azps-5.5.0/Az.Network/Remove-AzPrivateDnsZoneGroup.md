---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: 1012bd4da163b992aec049643feb1e3fd8b4bf76
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191729"
---
# <span data-ttu-id="a67c4-101">Remove-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="a67c4-101">Remove-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="a67c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a67c4-102">SYNOPSIS</span></span>
<span data-ttu-id="a67c4-103">DNS 영역 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a67c4-103">Removes a DNS zone group.</span></span>

## <span data-ttu-id="a67c4-104">구문</span><span class="sxs-lookup"><span data-stu-id="a67c4-104">SYNTAX</span></span>

```
Remove-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a67c4-105">설명</span><span class="sxs-lookup"><span data-stu-id="a67c4-105">DESCRIPTION</span></span>
<span data-ttu-id="a67c4-106">**Remove-AzPrivateDnsZoneGroup** cmdlet은 DNS 영역 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a67c4-106">The **Remove-AzPrivateDnsZoneGroup** cmdlet removes a DNS zone group.</span></span> 

## <span data-ttu-id="a67c4-107">예제</span><span class="sxs-lookup"><span data-stu-id="a67c4-107">EXAMPLES</span></span>

### <span data-ttu-id="a67c4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a67c4-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name dnsgroup1 
```

<span data-ttu-id="a67c4-109">위의 예제에서는 엔드포인트 test-pr-endpoint에서 dnsgroup1이라는 DNS 영역 grup을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a67c4-109">Above example removes a DNS zone grup named dnsgroup1 from endpoint test-pr-endpoint.</span></span>

## <span data-ttu-id="a67c4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a67c4-110">PARAMETERS</span></span>

### <span data-ttu-id="a67c4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a67c4-111">-AsJob</span></span>
<span data-ttu-id="a67c4-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a67c4-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a67c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a67c4-113">-DefaultProfile</span></span>
<span data-ttu-id="a67c4-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a67c4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a67c4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a67c4-115">-Force</span></span>
<span data-ttu-id="a67c4-116">리소스를 삭제하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a67c4-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="a67c4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a67c4-117">-Name</span></span>
<span data-ttu-id="a67c4-118">사설 dns 영역 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a67c4-118">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="a67c4-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a67c4-119">-PassThru</span></span>
<span data-ttu-id="a67c4-120">{{ PassThru 설명 채우기 }}</span><span class="sxs-lookup"><span data-stu-id="a67c4-120">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="a67c4-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="a67c4-121">-PrivateEndpointName</span></span>
<span data-ttu-id="a67c4-122">개인 엔드포인트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a67c4-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="a67c4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a67c4-123">-ResourceGroupName</span></span>
<span data-ttu-id="a67c4-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a67c4-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="a67c4-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a67c4-125">-Confirm</span></span>
<span data-ttu-id="a67c4-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a67c4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a67c4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a67c4-127">-WhatIf</span></span>
<span data-ttu-id="a67c4-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a67c4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a67c4-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a67c4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a67c4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a67c4-130">CommonParameters</span></span>
<span data-ttu-id="a67c4-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a67c4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a67c4-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a67c4-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a67c4-133">입력</span><span class="sxs-lookup"><span data-stu-id="a67c4-133">INPUTS</span></span>

### <span data-ttu-id="a67c4-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a67c4-134">System.String</span></span>

## <span data-ttu-id="a67c4-135">출력</span><span class="sxs-lookup"><span data-stu-id="a67c4-135">OUTPUTS</span></span>

### <span data-ttu-id="a67c4-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a67c4-136">System.Boolean</span></span>

## <span data-ttu-id="a67c4-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a67c4-137">NOTES</span></span>

## <span data-ttu-id="a67c4-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a67c4-138">RELATED LINKS</span></span>
