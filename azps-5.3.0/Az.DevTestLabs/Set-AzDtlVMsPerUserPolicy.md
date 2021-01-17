---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D00E04D9-C91F-4F89-8867-0A026C274F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: 48f9e2a91923fa123b54b5ebf09abbb7cd64a1dd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492033"
---
# <span data-ttu-id="9cdeb-101">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="9cdeb-101">Set-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="9cdeb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cdeb-102">SYNOPSIS</span></span>
<span data-ttu-id="9cdeb-103">DevTest Labs에서 랩의 사용자 정책당 가상 머신을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9cdeb-103">Sets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="9cdeb-104">구문</span><span class="sxs-lookup"><span data-stu-id="9cdeb-104">SYNTAX</span></span>

### <span data-ttu-id="9cdeb-105">사용(기본값)</span><span class="sxs-lookup"><span data-stu-id="9cdeb-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cdeb-106">사용 안</span><span class="sxs-lookup"><span data-stu-id="9cdeb-106">Disable</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cdeb-107">설명</span><span class="sxs-lookup"><span data-stu-id="9cdeb-107">DESCRIPTION</span></span>
<span data-ttu-id="9cdeb-108">**Set-AzDtlVMsPerUserPolicy** cmdlet은 랩의 사용자 정책당 가상 머신을 설정하여 사용자당 허용되는 최대 가상 머신 수를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9cdeb-108">The **Set-AzDtlVMsPerUserPolicy** cmdlet sets the virtual machines per user policy of a lab, which sets the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="9cdeb-109">cmdlet은 지정된 리소스 그룹 및 랩의 이름을 사용하여 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9cdeb-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="9cdeb-110">예제</span><span class="sxs-lookup"><span data-stu-id="9cdeb-110">EXAMPLES</span></span>

## <span data-ttu-id="9cdeb-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9cdeb-111">PARAMETERS</span></span>

### <span data-ttu-id="9cdeb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cdeb-112">-DefaultProfile</span></span>
<span data-ttu-id="9cdeb-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9cdeb-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9cdeb-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="9cdeb-114">-Disable</span></span>
<span data-ttu-id="9cdeb-115">이 cmdlet이 랩에 대한 정책을 사용하지 않도록 설정하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9cdeb-115">Indicates that this cmdlet disables the policy for the lab.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cdeb-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="9cdeb-116">-Enable</span></span>
<span data-ttu-id="9cdeb-117">이 cmdlet을 통해 랩에 대한 정책을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9cdeb-117">Indicates that this cmdlet enables the policy for the lab.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Enable
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cdeb-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="9cdeb-118">-LabName</span></span>
<span data-ttu-id="9cdeb-119">이 cmdlet이 사용자 정책당 가상 머신을 설정하는 랩의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9cdeb-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per user policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cdeb-120">-MaxVM</span><span class="sxs-lookup"><span data-stu-id="9cdeb-120">-MaxVMs</span></span>
<span data-ttu-id="9cdeb-121">랩에서 만들 수 있는 가상 머신의 최대 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9cdeb-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cdeb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cdeb-122">-ResourceGroupName</span></span>
<span data-ttu-id="9cdeb-123">랩이 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9cdeb-123">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cdeb-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9cdeb-124">-Confirm</span></span>
<span data-ttu-id="9cdeb-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9cdeb-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cdeb-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cdeb-126">-WhatIf</span></span>
<span data-ttu-id="9cdeb-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9cdeb-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cdeb-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9cdeb-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cdeb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cdeb-129">CommonParameters</span></span>
<span data-ttu-id="9cdeb-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9cdeb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cdeb-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9cdeb-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cdeb-132">입력</span><span class="sxs-lookup"><span data-stu-id="9cdeb-132">INPUTS</span></span>

### <span data-ttu-id="9cdeb-133">System.String</span><span class="sxs-lookup"><span data-stu-id="9cdeb-133">System.String</span></span>

## <span data-ttu-id="9cdeb-134">출력</span><span class="sxs-lookup"><span data-stu-id="9cdeb-134">OUTPUTS</span></span>

### <span data-ttu-id="9cdeb-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="9cdeb-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="9cdeb-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9cdeb-136">NOTES</span></span>

## <span data-ttu-id="9cdeb-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9cdeb-137">RELATED LINKS</span></span>

[<span data-ttu-id="9cdeb-138">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="9cdeb-138">Get-AzDtlVMsPerUserPolicy</span></span>](./Get-AzDtlVMsPerUserPolicy.md)


