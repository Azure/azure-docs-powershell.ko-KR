---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
ms.openlocfilehash: f7adb9ef086b233d44f2e5d9c6eb132669b102e5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048104"
---
# <span data-ttu-id="bf573-101">Update-AzVmssInstance</span><span class="sxs-lookup"><span data-stu-id="bf573-101">Update-AzVmssInstance</span></span>

## <span data-ttu-id="bf573-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf573-102">SYNOPSIS</span></span>
<span data-ttu-id="bf573-103">VMSS 인스턴스의 수동 업그레이드를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf573-103">Starts a manual upgrade of the VMSS instance.</span></span>

## <span data-ttu-id="bf573-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bf573-104">SYNTAX</span></span>

```
Update-AzVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf573-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bf573-105">DESCRIPTION</span></span>
<span data-ttu-id="bf573-106">Update-AzVmssInstance cmdlet은 지정 된 VMSS (가상 컴퓨터 크기 집합) 인스턴스의 수동 업그레이드를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf573-106">The Update-AzVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="bf573-107">이는 VMSS Scale 집합의 업그레이드 정책이 수동으로 설정 된 경우에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bf573-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="bf573-108">예제의</span><span class="sxs-lookup"><span data-stu-id="bf573-108">EXAMPLES</span></span>

### <span data-ttu-id="bf573-109">예제 1: VMSS 인스턴스의 업그레이드 시작</span><span class="sxs-lookup"><span data-stu-id="bf573-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="bf573-110">이 명령은 인스턴스 ID가 0 인 VMScaleSet001 이라는 VMSS의 업그레이드를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf573-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="bf573-111">변수</span><span class="sxs-lookup"><span data-stu-id="bf573-111">PARAMETERS</span></span>

### <span data-ttu-id="bf573-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf573-112">-AsJob</span></span>
<span data-ttu-id="bf573-113">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf573-113">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="bf573-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf573-114">-DefaultProfile</span></span>
<span data-ttu-id="bf573-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bf573-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf573-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="bf573-116">-InstanceId</span></span>
<span data-ttu-id="bf573-117">문자열 배열로 업그레이드할 인스턴스의 ID 또는 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf573-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf573-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf573-118">-ResourceGroupName</span></span>
<span data-ttu-id="bf573-119">VMSS의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf573-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="bf573-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="bf573-120">-VMScaleSetName</span></span>
<span data-ttu-id="bf573-121">이 cmdlet이 업그레이드 하는 VMSS 인스턴스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf573-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf573-122">-확인</span><span class="sxs-lookup"><span data-stu-id="bf573-122">-Confirm</span></span>
<span data-ttu-id="bf573-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf573-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf573-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf573-124">-WhatIf</span></span>
<span data-ttu-id="bf573-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bf573-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf573-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf573-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf573-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf573-127">CommonParameters</span></span>
<span data-ttu-id="bf573-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf573-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf573-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bf573-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf573-130">입력</span><span class="sxs-lookup"><span data-stu-id="bf573-130">INPUTS</span></span>

### <span data-ttu-id="bf573-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bf573-131">System.String</span></span>

### <span data-ttu-id="bf573-132">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="bf573-132">System.String[]</span></span>

## <span data-ttu-id="bf573-133">출력</span><span class="sxs-lookup"><span data-stu-id="bf573-133">OUTPUTS</span></span>

### <span data-ttu-id="bf573-134">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="bf573-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="bf573-135">상속자</span><span class="sxs-lookup"><span data-stu-id="bf573-135">NOTES</span></span>

## <span data-ttu-id="bf573-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bf573-136">RELATED LINKS</span></span>

[<span data-ttu-id="bf573-137">업데이트-AzVmss</span><span class="sxs-lookup"><span data-stu-id="bf573-137">Update-AzVmss</span></span>](./Update-AzVmss.md)


