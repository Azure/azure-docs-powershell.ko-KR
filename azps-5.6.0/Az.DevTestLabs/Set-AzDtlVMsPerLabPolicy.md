---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D2A7ECF6-E2B1-4BD5-BEA6-C9EC0C7377BA
online version: https://docs.microsoft.com/powershell/module/az.devtestlabs/set-azdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerLabPolicy.md
ms.openlocfilehash: 30aad11674cbdef747e444d18bce55ed223e3698
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010576"
---
# <span data-ttu-id="20c26-101">Set-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="20c26-101">Set-AzDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="20c26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20c26-102">SYNOPSIS</span></span>
<span data-ttu-id="20c26-103">DevTest Labs에서 랩당 가상 머신 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="20c26-103">Sets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="20c26-104">구문</span><span class="sxs-lookup"><span data-stu-id="20c26-104">SYNTAX</span></span>

### <span data-ttu-id="20c26-105">사용(기본값)</span><span class="sxs-lookup"><span data-stu-id="20c26-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20c26-106">사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="20c26-106">Disable</span></span>
```
Set-AzDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20c26-107">설명</span><span class="sxs-lookup"><span data-stu-id="20c26-107">DESCRIPTION</span></span>
<span data-ttu-id="20c26-108">**Set-AzDtlVMsPerLabPolicy** cmdlet은 랩의 랩 정책당 가상 머신을 설정하여 랩에서 허용되는 총 가상 머신 수를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="20c26-108">The **Set-AzDtlVMsPerLabPolicy** cmdlet sets the virtual machines per lab policy of a lab, which sets the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="20c26-109">cmdlet은 랩의 지정된 리소스 그룹 및 이름을 사용하여 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="20c26-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="20c26-110">예제</span><span class="sxs-lookup"><span data-stu-id="20c26-110">EXAMPLES</span></span>

## <span data-ttu-id="20c26-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="20c26-111">PARAMETERS</span></span>

### <span data-ttu-id="20c26-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20c26-112">-DefaultProfile</span></span>
<span data-ttu-id="20c26-113">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="20c26-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20c26-114">-사용 안</span><span class="sxs-lookup"><span data-stu-id="20c26-114">-Disable</span></span>
<span data-ttu-id="20c26-115">이 cmdlet이 랩의 정책을 사용하지 않도록 설정하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20c26-115">Indicates that this cmdlet disables the policy of the lab.</span></span>

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

### <span data-ttu-id="20c26-116">-사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="20c26-116">-Enable</span></span>
<span data-ttu-id="20c26-117">이 cmdlet이 랩의 정책을 가능하게 하여 를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="20c26-117">Indicates that this cmdlet enables the policy of the lab.</span></span>

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

### <span data-ttu-id="20c26-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="20c26-118">-LabName</span></span>
<span data-ttu-id="20c26-119">이 cmdlet이 랩 정책당 가상 머신을 설정하는 랩 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="20c26-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per lab policy.</span></span>

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

### <span data-ttu-id="20c26-120">-MaxVM</span><span class="sxs-lookup"><span data-stu-id="20c26-120">-MaxVMs</span></span>
<span data-ttu-id="20c26-121">랩에서 만들 수 있는 가상 머신의 최대 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="20c26-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

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

### <span data-ttu-id="20c26-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20c26-122">-ResourceGroupName</span></span>
<span data-ttu-id="20c26-123">랩이 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="20c26-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="20c26-124">-확인</span><span class="sxs-lookup"><span data-stu-id="20c26-124">-Confirm</span></span>
<span data-ttu-id="20c26-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="20c26-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20c26-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20c26-126">-WhatIf</span></span>
<span data-ttu-id="20c26-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="20c26-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20c26-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="20c26-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20c26-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20c26-129">CommonParameters</span></span>
<span data-ttu-id="20c26-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="20c26-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20c26-131">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="20c26-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20c26-132">입력</span><span class="sxs-lookup"><span data-stu-id="20c26-132">INPUTS</span></span>

### <span data-ttu-id="20c26-133">System.String</span><span class="sxs-lookup"><span data-stu-id="20c26-133">System.String</span></span>

## <span data-ttu-id="20c26-134">출력</span><span class="sxs-lookup"><span data-stu-id="20c26-134">OUTPUTS</span></span>

### <span data-ttu-id="20c26-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="20c26-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="20c26-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="20c26-136">NOTES</span></span>

## <span data-ttu-id="20c26-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20c26-137">RELATED LINKS</span></span>

[<span data-ttu-id="20c26-138">Get-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="20c26-138">Get-AzDtlVMsPerLabPolicy</span></span>](./Get-AzDtlVMsPerLabPolicy.md)


