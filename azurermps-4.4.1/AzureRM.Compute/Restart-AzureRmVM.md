---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVM.md
ms.openlocfilehash: 5a848c2e4a13df6a38c67e067531ff8581bd595e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525620"
---
# <span data-ttu-id="eee04-101">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="eee04-101">Restart-AzureRmVM</span></span>

## <span data-ttu-id="eee04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eee04-102">SYNOPSIS</span></span>
<span data-ttu-id="eee04-103">Azure 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee04-103">Restarts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eee04-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eee04-104">SYNTAX</span></span>

### <span data-ttu-id="eee04-105">RestartResourceGroupNameParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="eee04-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eee04-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="eee04-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eee04-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="eee04-107">RestartIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eee04-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="eee04-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-PerformMaintenance]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eee04-109">설명은</span><span class="sxs-lookup"><span data-stu-id="eee04-109">DESCRIPTION</span></span>
<span data-ttu-id="eee04-110">**AzureRmVM** Cmdlet은 Azure 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee04-110">The **Restart-AzureRmVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="eee04-111">예제의</span><span class="sxs-lookup"><span data-stu-id="eee04-111">EXAMPLES</span></span>

### <span data-ttu-id="eee04-112">예제 1: 가상 컴퓨터 다시 시작</span><span class="sxs-lookup"><span data-stu-id="eee04-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="eee04-113">이 명령은 ResourceGroup11에서 VirtualMachine07 이라는 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee04-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="eee04-114">변수</span><span class="sxs-lookup"><span data-stu-id="eee04-114">PARAMETERS</span></span>

### <span data-ttu-id="eee04-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eee04-115">-DefaultProfile</span></span>
<span data-ttu-id="eee04-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eee04-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eee04-117">-Id</span><span class="sxs-lookup"><span data-stu-id="eee04-117">-Id</span></span>
<span data-ttu-id="eee04-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eee04-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eee04-119">-이름</span><span class="sxs-lookup"><span data-stu-id="eee04-119">-Name</span></span>
<span data-ttu-id="eee04-120">가상 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eee04-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="eee04-121">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="eee04-121">-PerformMaintenance</span></span>
<span data-ttu-id="eee04-122">가상 컴퓨터의 유지 관리를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee04-122">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eee04-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eee04-123">-ResourceGroupName</span></span>
<span data-ttu-id="eee04-124">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee04-124">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eee04-125">-확인</span><span class="sxs-lookup"><span data-stu-id="eee04-125">-Confirm</span></span>
<span data-ttu-id="eee04-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee04-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eee04-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eee04-127">-WhatIf</span></span>
<span data-ttu-id="eee04-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="eee04-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eee04-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eee04-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eee04-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eee04-130">CommonParameters</span></span>
<span data-ttu-id="eee04-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee04-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eee04-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eee04-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eee04-133">입력</span><span class="sxs-lookup"><span data-stu-id="eee04-133">INPUTS</span></span>

## <span data-ttu-id="eee04-134">출력</span><span class="sxs-lookup"><span data-stu-id="eee04-134">OUTPUTS</span></span>

## <span data-ttu-id="eee04-135">상속자</span><span class="sxs-lookup"><span data-stu-id="eee04-135">NOTES</span></span>

## <span data-ttu-id="eee04-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eee04-136">RELATED LINKS</span></span>

[<span data-ttu-id="eee04-137">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="eee04-137">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="eee04-138">새로운 AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="eee04-138">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="eee04-139">제거-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="eee04-139">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="eee04-140">시작-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="eee04-140">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="eee04-141">중지-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="eee04-141">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="eee04-142">업데이트-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="eee04-142">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


