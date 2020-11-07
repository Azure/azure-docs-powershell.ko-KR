---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: D2A7ECF6-E2B1-4BD5-BEA6-C9EC0C7377BA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/set-azurermdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerLabPolicy.md
ms.openlocfilehash: 8e6e50fd22330073d647353232c549579aa382a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703063"
---
# <span data-ttu-id="f3d80-101">Set-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="f3d80-101">Set-AzureRmDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="f3d80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3d80-102">SYNOPSIS</span></span>
<span data-ttu-id="f3d80-103">DevTest 랩에서 랩에 대 한 랩 정책에 따라 가상 컴퓨터를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3d80-103">Sets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3d80-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f3d80-104">SYNTAX</span></span>

### <span data-ttu-id="f3d80-105">사용 (기본값)</span><span class="sxs-lookup"><span data-stu-id="f3d80-105">Enable (Default)</span></span>
```
Set-AzureRmDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3d80-106">설정할</span><span class="sxs-lookup"><span data-stu-id="f3d80-106">Disable</span></span>
```
Set-AzureRmDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3d80-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f3d80-107">DESCRIPTION</span></span>
<span data-ttu-id="f3d80-108">**AzureRmDtlVMsPerLabPolicy** cmdlet은 랩에서 사용할 수 있는 가상 컴퓨터의 총 수를 설정 하는 랩의 랩 정책 당 가상 컴퓨터를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3d80-108">The **Set-AzureRmDtlVMsPerLabPolicy** cmdlet sets the virtual machines per lab policy of a lab, which sets the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="f3d80-109">Cmdlet은 지정 된 리소스 그룹 및 랩의 이름을 사용 하 여 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3d80-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="f3d80-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f3d80-110">EXAMPLES</span></span>

## <span data-ttu-id="f3d80-111">변수</span><span class="sxs-lookup"><span data-stu-id="f3d80-111">PARAMETERS</span></span>

### <span data-ttu-id="f3d80-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3d80-112">-DefaultProfile</span></span>
<span data-ttu-id="f3d80-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f3d80-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3d80-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="f3d80-114">-Disable</span></span>
<span data-ttu-id="f3d80-115">이 cmdlet이 랩의 정책을 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3d80-115">Indicates that this cmdlet disables the policy of the lab.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Disable
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3d80-116">-사용</span><span class="sxs-lookup"><span data-stu-id="f3d80-116">-Enable</span></span>
<span data-ttu-id="f3d80-117">이 cmdlet이 랩의 정책을 사용할 수 있도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3d80-117">Indicates that this cmdlet enables the policy of the lab.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Enable
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3d80-118">-시 이름</span><span class="sxs-lookup"><span data-stu-id="f3d80-118">-LabName</span></span>
<span data-ttu-id="f3d80-119">이 cmdlet이 랩 정책 당 가상 컴퓨터를 설정 하는 랩의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3d80-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per lab policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3d80-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="f3d80-120">-MaxVMs</span></span>
<span data-ttu-id="f3d80-121">랩에서 만들 수 있는 최대 가상 컴퓨터 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3d80-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3d80-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3d80-122">-ResourceGroupName</span></span>
<span data-ttu-id="f3d80-123">랩이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3d80-123">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3d80-124">-확인</span><span class="sxs-lookup"><span data-stu-id="f3d80-124">-Confirm</span></span>
<span data-ttu-id="f3d80-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3d80-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3d80-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3d80-126">-WhatIf</span></span>
<span data-ttu-id="f3d80-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f3d80-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3d80-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f3d80-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3d80-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3d80-129">CommonParameters</span></span>
<span data-ttu-id="f3d80-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3d80-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3d80-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3d80-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3d80-132">입력</span><span class="sxs-lookup"><span data-stu-id="f3d80-132">INPUTS</span></span>

### <span data-ttu-id="f3d80-133">않아야</span><span class="sxs-lookup"><span data-stu-id="f3d80-133">None</span></span>
<span data-ttu-id="f3d80-134">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f3d80-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f3d80-135">출력</span><span class="sxs-lookup"><span data-stu-id="f3d80-135">OUTPUTS</span></span>

### <span data-ttu-id="f3d80-136">Microsoft. DevTestLabs. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="f3d80-136">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="f3d80-137">이 cmdlet은 랩에서 만들 수 있는 최대 가상 컴퓨터 수를 지정 하는 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3d80-137">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created in the lab.</span></span>

## <span data-ttu-id="f3d80-138">상속자</span><span class="sxs-lookup"><span data-stu-id="f3d80-138">NOTES</span></span>

## <span data-ttu-id="f3d80-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3d80-139">RELATED LINKS</span></span>

[<span data-ttu-id="f3d80-140">Get-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="f3d80-140">Get-AzureRmDtlVMsPerLabPolicy</span></span>](./Get-AzureRmDtlVMsPerLabPolicy.md)


