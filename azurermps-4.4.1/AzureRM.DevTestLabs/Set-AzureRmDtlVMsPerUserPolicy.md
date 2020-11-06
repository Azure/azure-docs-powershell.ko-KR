---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: D00E04D9-C91F-4F89-8867-0A026C274F27
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerUserPolicy.md
ms.openlocfilehash: b3790105f2404cc7bf50ef1200ce0978e8f0b15d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534104"
---
# <span data-ttu-id="0212f-101">Set-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="0212f-101">Set-AzureRmDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="0212f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0212f-102">SYNOPSIS</span></span>
<span data-ttu-id="0212f-103">DevTest 랩에서 랩에서 사용자 별 가상 컴퓨터 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0212f-103">Sets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0212f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0212f-104">SYNTAX</span></span>

### <span data-ttu-id="0212f-105">사용 (기본값)</span><span class="sxs-lookup"><span data-stu-id="0212f-105">Enable (Default)</span></span>
```
Set-AzureRmDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0212f-106">설정할</span><span class="sxs-lookup"><span data-stu-id="0212f-106">Disable</span></span>
```
Set-AzureRmDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0212f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0212f-107">DESCRIPTION</span></span>
<span data-ttu-id="0212f-108">**AzureRmDtlVMsPerUserPolicy** cmdlet은 사용자 당 허용 되는 최대 가상 컴퓨터 수를 설정 하는 랩의 사용자 정책 당 가상 컴퓨터를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0212f-108">The **Set-AzureRmDtlVMsPerUserPolicy** cmdlet sets the virtual machines per user policy of a lab, which sets the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="0212f-109">Cmdlet은 지정 된 리소스 그룹 및 랩의 이름을 사용 하 여 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0212f-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="0212f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0212f-110">EXAMPLES</span></span>

## <span data-ttu-id="0212f-111">변수</span><span class="sxs-lookup"><span data-stu-id="0212f-111">PARAMETERS</span></span>

### <span data-ttu-id="0212f-112">-Disable</span><span class="sxs-lookup"><span data-stu-id="0212f-112">-Disable</span></span>
<span data-ttu-id="0212f-113">이 cmdlet이 랩에 대 한 정책을 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0212f-113">Indicates that this cmdlet disables the policy for the lab.</span></span>

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

### <span data-ttu-id="0212f-114">-사용</span><span class="sxs-lookup"><span data-stu-id="0212f-114">-Enable</span></span>
<span data-ttu-id="0212f-115">이 cmdlet이 랩에 대 한 정책을 사용할 수 있도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0212f-115">Indicates that this cmdlet enables the policy for the lab.</span></span>

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

### <span data-ttu-id="0212f-116">-시 이름</span><span class="sxs-lookup"><span data-stu-id="0212f-116">-LabName</span></span>
<span data-ttu-id="0212f-117">이 cmdlet이 사용자 정책 당 가상 컴퓨터를 설정 하는 랩의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0212f-117">Specifies the name of the lab for which this cmdlet sets the virtual machines per user policy.</span></span>

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

### <span data-ttu-id="0212f-118">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="0212f-118">-MaxVMs</span></span>
<span data-ttu-id="0212f-119">랩에서 만들 수 있는 최대 가상 컴퓨터 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0212f-119">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

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

### <span data-ttu-id="0212f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0212f-120">-ResourceGroupName</span></span>
<span data-ttu-id="0212f-121">랩이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0212f-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="0212f-122">-확인</span><span class="sxs-lookup"><span data-stu-id="0212f-122">-Confirm</span></span>
<span data-ttu-id="0212f-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0212f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0212f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0212f-124">-WhatIf</span></span>
<span data-ttu-id="0212f-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0212f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0212f-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0212f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0212f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0212f-127">-DefaultProfile</span></span>
<span data-ttu-id="0212f-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0212f-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0212f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0212f-129">CommonParameters</span></span>
<span data-ttu-id="0212f-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0212f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0212f-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0212f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0212f-132">입력</span><span class="sxs-lookup"><span data-stu-id="0212f-132">INPUTS</span></span>

## <span data-ttu-id="0212f-133">출력</span><span class="sxs-lookup"><span data-stu-id="0212f-133">OUTPUTS</span></span>

### <span data-ttu-id="0212f-134">Microsoft. DevTestLabs. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="0212f-134">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="0212f-135">이 cmdlet은 랩에서 사용자가 만들 수 있는 최대 가상 컴퓨터 수를 지정 하는 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0212f-135">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created by a user in the lab.</span></span>

## <span data-ttu-id="0212f-136">상속자</span><span class="sxs-lookup"><span data-stu-id="0212f-136">NOTES</span></span>

## <span data-ttu-id="0212f-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0212f-137">RELATED LINKS</span></span>

[<span data-ttu-id="0212f-138">Get-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="0212f-138">Get-AzureRmDtlVMsPerUserPolicy</span></span>](./Get-AzureRmDtlVMsPerUserPolicy.md)


