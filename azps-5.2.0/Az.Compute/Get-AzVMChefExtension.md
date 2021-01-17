---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
ms.openlocfilehash: 02647fc2148069e2c408c979e4b258fd0a641fc0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347733"
---
# <span data-ttu-id="35e19-101">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="35e19-101">Get-AzVMChefExtension</span></span>

## <span data-ttu-id="35e19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35e19-102">SYNOPSIS</span></span>
<span data-ttu-id="35e19-103">Chef 확장에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="35e19-103">Gets information about a Chef extension.</span></span>

## <span data-ttu-id="35e19-104">구문</span><span class="sxs-lookup"><span data-stu-id="35e19-104">SYNTAX</span></span>

### <span data-ttu-id="35e19-105">Linux</span><span class="sxs-lookup"><span data-stu-id="35e19-105">Linux</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35e19-106">Windows</span><span class="sxs-lookup"><span data-stu-id="35e19-106">Windows</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35e19-107">설명</span><span class="sxs-lookup"><span data-stu-id="35e19-107">DESCRIPTION</span></span>
<span data-ttu-id="35e19-108">**Get-AzVMChefExtension** cmdlet은 가상 머신에 설치된 Chef 확장에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="35e19-108">The **Get-AzVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="35e19-109">예제</span><span class="sxs-lookup"><span data-stu-id="35e19-109">EXAMPLES</span></span>

### <span data-ttu-id="35e19-110">예제 1: Windows 가상 머신에 대한 Chef 확장에 대한 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="35e19-110">Example 1: Get the details of Chef extension for a Windows virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="35e19-111">이 명령은 ResourceGroup001이라는 리소스 그룹에 속하는 WindowsVM001이라는 Windows 가상 머신에서 Chef 확장을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="35e19-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="35e19-112">예제 2: Linux 가상 머신에 대한 Chef 확장에 대한 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="35e19-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="35e19-113">이 명령은 ResourceGroup002라는 리소스 그룹에 속하는 LinuxVM001이라는 Linux 가상 머신에서 Chef 확장을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="35e19-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="35e19-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35e19-114">PARAMETERS</span></span>

### <span data-ttu-id="35e19-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35e19-115">-DefaultProfile</span></span>
<span data-ttu-id="35e19-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="35e19-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35e19-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="35e19-117">-Linux</span></span>
<span data-ttu-id="35e19-118">이 cmdlet이 Linux 가상 머신에서 작동하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="35e19-118">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

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

### <span data-ttu-id="35e19-119">-Name</span><span class="sxs-lookup"><span data-stu-id="35e19-119">-Name</span></span>
<span data-ttu-id="35e19-120">Chef 확장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="35e19-120">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="35e19-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35e19-121">-ResourceGroupName</span></span>
<span data-ttu-id="35e19-122">가상 머신을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="35e19-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="35e19-123">-Status</span><span class="sxs-lookup"><span data-stu-id="35e19-123">-Status</span></span>
<span data-ttu-id="35e19-124">이 cmdlet은 Chef 확장의 인스턴스 보기만 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="35e19-124">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

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

### <span data-ttu-id="35e19-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="35e19-125">-VMName</span></span>
<span data-ttu-id="35e19-126">가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="35e19-126">Specifies the name of a virtual machine.</span></span>

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

### <span data-ttu-id="35e19-127">-Windows</span><span class="sxs-lookup"><span data-stu-id="35e19-127">-Windows</span></span>
<span data-ttu-id="35e19-128">이 cmdlet이 Windows 가상 머신에 대한 것일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35e19-128">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

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

### <span data-ttu-id="35e19-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35e19-129">CommonParameters</span></span>
<span data-ttu-id="35e19-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="35e19-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35e19-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="35e19-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35e19-132">입력</span><span class="sxs-lookup"><span data-stu-id="35e19-132">INPUTS</span></span>

### <span data-ttu-id="35e19-133">System.String</span><span class="sxs-lookup"><span data-stu-id="35e19-133">System.String</span></span>

### <span data-ttu-id="35e19-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="35e19-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="35e19-135">출력</span><span class="sxs-lookup"><span data-stu-id="35e19-135">OUTPUTS</span></span>

### <span data-ttu-id="35e19-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="35e19-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="35e19-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="35e19-137">NOTES</span></span>

## <span data-ttu-id="35e19-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35e19-138">RELATED LINKS</span></span>

[<span data-ttu-id="35e19-139">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="35e19-139">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)

[<span data-ttu-id="35e19-140">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="35e19-140">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)


