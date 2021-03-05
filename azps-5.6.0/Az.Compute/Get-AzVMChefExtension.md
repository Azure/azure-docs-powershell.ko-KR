---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
ms.openlocfilehash: c0d672636d273bcd6e1d2c5f3ebc1c3b70a7b208
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013856"
---
# <span data-ttu-id="247ae-101">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="247ae-101">Get-AzVMChefExtension</span></span>

## <span data-ttu-id="247ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="247ae-102">SYNOPSIS</span></span>
<span data-ttu-id="247ae-103">Chef 확장에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="247ae-103">Gets information about a Chef extension.</span></span>

## <span data-ttu-id="247ae-104">구문</span><span class="sxs-lookup"><span data-stu-id="247ae-104">SYNTAX</span></span>

### <span data-ttu-id="247ae-105">Linux</span><span class="sxs-lookup"><span data-stu-id="247ae-105">Linux</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="247ae-106">Windows</span><span class="sxs-lookup"><span data-stu-id="247ae-106">Windows</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="247ae-107">설명</span><span class="sxs-lookup"><span data-stu-id="247ae-107">DESCRIPTION</span></span>
<span data-ttu-id="247ae-108">**Get-AzVMChefExtension** cmdlet은 가상 머신에 설치된 Chef 확장에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="247ae-108">The **Get-AzVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="247ae-109">예제</span><span class="sxs-lookup"><span data-stu-id="247ae-109">EXAMPLES</span></span>

### <span data-ttu-id="247ae-110">예제 1: Windows 가상 머신에 대한 Chef 확장에 대한 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="247ae-110">Example 1: Get the details of Chef extension for a Windows virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="247ae-111">이 명령은 ResourceGroup001이라는 리소스 그룹에 속하는 WindowsVM001이라는 Windows 가상 머신에서 Chef 확장을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="247ae-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="247ae-112">예제 2: Linux 가상 머신에 대한 Chef 확장에 대한 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="247ae-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="247ae-113">이 명령은 ResourceGroup002라는 리소스 그룹에 속하는 LinuxVM001이라는 Linux 가상 머신에서 Chef 확장을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="247ae-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="247ae-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="247ae-114">PARAMETERS</span></span>

### <span data-ttu-id="247ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="247ae-115">-DefaultProfile</span></span>
<span data-ttu-id="247ae-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="247ae-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="247ae-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="247ae-117">-Linux</span></span>
<span data-ttu-id="247ae-118">이 cmdlet은 Linux 가상 머신에서 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="247ae-118">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="247ae-119">-Name</span><span class="sxs-lookup"><span data-stu-id="247ae-119">-Name</span></span>
<span data-ttu-id="247ae-120">Chef 확장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="247ae-120">Specifies the name of the Chef extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="247ae-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="247ae-121">-ResourceGroupName</span></span>
<span data-ttu-id="247ae-122">가상 머신을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="247ae-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="247ae-123">-Status</span><span class="sxs-lookup"><span data-stu-id="247ae-123">-Status</span></span>
<span data-ttu-id="247ae-124">이 cmdlet은 Chef 확장의 인스턴스 보기만 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="247ae-124">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="247ae-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="247ae-125">-VMName</span></span>
<span data-ttu-id="247ae-126">가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="247ae-126">Specifies the name of a virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="247ae-127">-Windows</span><span class="sxs-lookup"><span data-stu-id="247ae-127">-Windows</span></span>
<span data-ttu-id="247ae-128">이 cmdlet은 Windows 가상 머신용입니다.</span><span class="sxs-lookup"><span data-stu-id="247ae-128">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="247ae-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="247ae-129">CommonParameters</span></span>
<span data-ttu-id="247ae-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="247ae-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="247ae-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="247ae-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="247ae-132">입력</span><span class="sxs-lookup"><span data-stu-id="247ae-132">INPUTS</span></span>

### <span data-ttu-id="247ae-133">System.String</span><span class="sxs-lookup"><span data-stu-id="247ae-133">System.String</span></span>

### <span data-ttu-id="247ae-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="247ae-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="247ae-135">출력</span><span class="sxs-lookup"><span data-stu-id="247ae-135">OUTPUTS</span></span>

### <span data-ttu-id="247ae-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="247ae-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="247ae-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="247ae-137">NOTES</span></span>

## <span data-ttu-id="247ae-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="247ae-138">RELATED LINKS</span></span>

[<span data-ttu-id="247ae-139">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="247ae-139">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)

[<span data-ttu-id="247ae-140">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="247ae-140">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)


