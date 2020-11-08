---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D2A7ECF6-E2B1-4BD5-BEA6-C9EC0C7377BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerLabPolicy.md
ms.openlocfilehash: 3e06b4f1236863e208a167024e9d0562dc82ca89
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042383"
---
# <span data-ttu-id="e25c9-101">Set-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="e25c9-101">Set-AzDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="e25c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e25c9-102">SYNOPSIS</span></span>
<span data-ttu-id="e25c9-103">DevTest 랩에서 랩에 대 한 랩 정책에 따라 가상 컴퓨터를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25c9-103">Sets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="e25c9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e25c9-104">SYNTAX</span></span>

### <span data-ttu-id="e25c9-105">사용 (기본값)</span><span class="sxs-lookup"><span data-stu-id="e25c9-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e25c9-106">설정할</span><span class="sxs-lookup"><span data-stu-id="e25c9-106">Disable</span></span>
```
Set-AzDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e25c9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e25c9-107">DESCRIPTION</span></span>
<span data-ttu-id="e25c9-108">**AzDtlVMsPerLabPolicy** cmdlet은 랩에서 사용할 수 있는 가상 컴퓨터의 총 수를 설정 하는 랩의 랩 정책 당 가상 컴퓨터를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25c9-108">The **Set-AzDtlVMsPerLabPolicy** cmdlet sets the virtual machines per lab policy of a lab, which sets the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="e25c9-109">Cmdlet은 지정 된 리소스 그룹 및 랩의 이름을 사용 하 여 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25c9-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="e25c9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e25c9-110">EXAMPLES</span></span>

## <span data-ttu-id="e25c9-111">변수</span><span class="sxs-lookup"><span data-stu-id="e25c9-111">PARAMETERS</span></span>

### <span data-ttu-id="e25c9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e25c9-112">-DefaultProfile</span></span>
<span data-ttu-id="e25c9-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e25c9-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e25c9-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="e25c9-114">-Disable</span></span>
<span data-ttu-id="e25c9-115">이 cmdlet이 랩의 정책을 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25c9-115">Indicates that this cmdlet disables the policy of the lab.</span></span>

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

### <span data-ttu-id="e25c9-116">-사용</span><span class="sxs-lookup"><span data-stu-id="e25c9-116">-Enable</span></span>
<span data-ttu-id="e25c9-117">이 cmdlet이 랩의 정책을 사용할 수 있도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25c9-117">Indicates that this cmdlet enables the policy of the lab.</span></span>

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

### <span data-ttu-id="e25c9-118">-시 이름</span><span class="sxs-lookup"><span data-stu-id="e25c9-118">-LabName</span></span>
<span data-ttu-id="e25c9-119">이 cmdlet이 랩 정책 당 가상 컴퓨터를 설정 하는 랩의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25c9-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per lab policy.</span></span>

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

### <span data-ttu-id="e25c9-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="e25c9-120">-MaxVMs</span></span>
<span data-ttu-id="e25c9-121">랩에서 만들 수 있는 최대 가상 컴퓨터 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25c9-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

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

### <span data-ttu-id="e25c9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e25c9-122">-ResourceGroupName</span></span>
<span data-ttu-id="e25c9-123">랩이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25c9-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="e25c9-124">-확인</span><span class="sxs-lookup"><span data-stu-id="e25c9-124">-Confirm</span></span>
<span data-ttu-id="e25c9-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25c9-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e25c9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e25c9-126">-WhatIf</span></span>
<span data-ttu-id="e25c9-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e25c9-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e25c9-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e25c9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e25c9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e25c9-129">CommonParameters</span></span>
<span data-ttu-id="e25c9-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25c9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e25c9-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e25c9-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e25c9-132">입력</span><span class="sxs-lookup"><span data-stu-id="e25c9-132">INPUTS</span></span>

### <span data-ttu-id="e25c9-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e25c9-133">System.String</span></span>

## <span data-ttu-id="e25c9-134">출력</span><span class="sxs-lookup"><span data-stu-id="e25c9-134">OUTPUTS</span></span>

### <span data-ttu-id="e25c9-135">Microsoft. DevTestLabs. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="e25c9-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="e25c9-136">상속자</span><span class="sxs-lookup"><span data-stu-id="e25c9-136">NOTES</span></span>

## <span data-ttu-id="e25c9-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e25c9-137">RELATED LINKS</span></span>

[<span data-ttu-id="e25c9-138">Get-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="e25c9-138">Get-AzDtlVMsPerLabPolicy</span></span>](./Get-AzDtlVMsPerLabPolicy.md)


