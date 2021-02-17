---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmbootdiagnosticsdata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
ms.openlocfilehash: ee210b5b9408f3de2b9e92213fafe4846ea8c3e1
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407100"
---
# <span data-ttu-id="e431d-101">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="e431d-101">Get-AzVMBootDiagnosticsData</span></span>

## <span data-ttu-id="e431d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e431d-102">SYNOPSIS</span></span>
<span data-ttu-id="e431d-103">가상 머신에 대한 부팅 진단 데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e431d-103">Gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="e431d-104">구문</span><span class="sxs-lookup"><span data-stu-id="e431d-104">SYNTAX</span></span>

### <span data-ttu-id="e431d-105">WindowsParamSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e431d-105">WindowsParamSet (Default)</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows] [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e431d-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="e431d-106">LinuxParamSet</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux] [[-LocalPath] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e431d-107">설명</span><span class="sxs-lookup"><span data-stu-id="e431d-107">DESCRIPTION</span></span>
<span data-ttu-id="e431d-108">**Get-AzVMBootDiagnosticsData** cmdlet은 가상 머신에 대한 부팅 진단 데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e431d-108">The **Get-AzVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="e431d-109">예제</span><span class="sxs-lookup"><span data-stu-id="e431d-109">EXAMPLES</span></span>

### <span data-ttu-id="e431d-110">예제 1: 부팅 진단 데이터 얻기</span><span class="sxs-lookup"><span data-stu-id="e431d-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="e431d-111">이 명령은 ContosoVM07이라는 가상 머신에 대한 부팅 진단 데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e431d-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="e431d-112">이 가상 머신은 Windows 운영 체제를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e431d-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="e431d-113">이 명령은 지정된 로컬 경로에 데이터를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e431d-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="e431d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e431d-114">PARAMETERS</span></span>

### <span data-ttu-id="e431d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e431d-115">-DefaultProfile</span></span>
<span data-ttu-id="e431d-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e431d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e431d-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="e431d-117">-Linux</span></span>
<span data-ttu-id="e431d-118">가상 머신이 Linux 운영 체제를 실행하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e431d-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LinuxParamSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e431d-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="e431d-119">-LocalPath</span></span>
<span data-ttu-id="e431d-120">부팅 진단 데이터에 대한 로컬 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e431d-120">Specifies the local path for the boot diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsParamSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: LinuxParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e431d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e431d-121">-Name</span></span>
<span data-ttu-id="e431d-122">이 cmdlet이 진단 데이터를 얻을 가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e431d-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e431d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e431d-123">-ResourceGroupName</span></span>
<span data-ttu-id="e431d-124">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e431d-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="e431d-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="e431d-125">-Windows</span></span>
<span data-ttu-id="e431d-126">가상 머신이 Windows 운영 체제를 실행하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e431d-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsParamSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e431d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e431d-127">CommonParameters</span></span>
<span data-ttu-id="e431d-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e431d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e431d-129">자세한 내용은 [다음](https://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e431d-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e431d-130">입력</span><span class="sxs-lookup"><span data-stu-id="e431d-130">INPUTS</span></span>

### <span data-ttu-id="e431d-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e431d-131">System.String</span></span>

## <span data-ttu-id="e431d-132">출력</span><span class="sxs-lookup"><span data-stu-id="e431d-132">OUTPUTS</span></span>

### <span data-ttu-id="e431d-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e431d-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="e431d-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="e431d-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="e431d-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e431d-135">NOTES</span></span>

## <span data-ttu-id="e431d-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e431d-136">RELATED LINKS</span></span>

[<span data-ttu-id="e431d-137">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e431d-137">Set-AzVMBootDiagnostic</span></span>](./Set-AzVMBootDiagnostic.md)


