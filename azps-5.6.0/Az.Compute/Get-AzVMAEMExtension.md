---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
ms.openlocfilehash: ed5f79763d8e9786f0a502f404474eeef2f641f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958992"
---
# <span data-ttu-id="1605d-101">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="1605d-101">Get-AzVMAEMExtension</span></span>

## <span data-ttu-id="1605d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1605d-102">SYNOPSIS</span></span>
<span data-ttu-id="1605d-103">AEM 확장에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1605d-103">Gets information about the AEM extension.</span></span>

## <span data-ttu-id="1605d-104">구문</span><span class="sxs-lookup"><span data-stu-id="1605d-104">SYNTAX</span></span>

```
Get-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1605d-105">설명</span><span class="sxs-lookup"><span data-stu-id="1605d-105">DESCRIPTION</span></span>
<span data-ttu-id="1605d-106">**Get-AzVMAEMExtension** cmdlet은 AEM(Azure Enhanced Monitoring) 확장에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1605d-106">The **Get-AzVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="1605d-107">예제</span><span class="sxs-lookup"><span data-stu-id="1605d-107">EXAMPLES</span></span>

### <span data-ttu-id="1605d-108">예제 1: AEM 확장 사용</span><span class="sxs-lookup"><span data-stu-id="1605d-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="1605d-109">이 명령은 contoso-server라는 가상 머신에 대한 AEM 확장에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1605d-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="1605d-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1605d-110">PARAMETERS</span></span>

### <span data-ttu-id="1605d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1605d-111">-DefaultProfile</span></span>
<span data-ttu-id="1605d-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1605d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1605d-113">-Name</span><span class="sxs-lookup"><span data-stu-id="1605d-113">-Name</span></span>
<span data-ttu-id="1605d-114">가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1605d-114">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="1605d-115">이 cmdlet은 이 cmdlet이 지정하는 가상 머신의 AEM 확장에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1605d-115">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="1605d-116">-OSType</span><span class="sxs-lookup"><span data-stu-id="1605d-116">-OSType</span></span>
<span data-ttu-id="1605d-117">운영 체제 디스크의 운영 체제 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1605d-117">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="1605d-118">운영 체제 디스크에 형식이 없는 경우 이 매개 변수를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1605d-118">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="1605d-119">이 매개 변수에 대해 허용되는 값은 Windows 및 Linux입니다.</span><span class="sxs-lookup"><span data-stu-id="1605d-119">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1605d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1605d-120">-ResourceGroupName</span></span>
<span data-ttu-id="1605d-121">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1605d-121">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="1605d-122">이 cmdlet은 해당 가상 머신의 AEM 확장에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1605d-122">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="1605d-123">-Status</span><span class="sxs-lookup"><span data-stu-id="1605d-123">-Status</span></span>
<span data-ttu-id="1605d-124">이 cmdlet은 AEM 확장의 인스턴스 보기만 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1605d-124">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

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

### <span data-ttu-id="1605d-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="1605d-125">-VMName</span></span>
<span data-ttu-id="1605d-126">가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1605d-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="1605d-127">이 cmdlet은 이 매개 변수가 지정하는 가상 머신에 대한 AEM 확장에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="1605d-127">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="1605d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1605d-128">CommonParameters</span></span>
<span data-ttu-id="1605d-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1605d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1605d-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1605d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1605d-131">입력</span><span class="sxs-lookup"><span data-stu-id="1605d-131">INPUTS</span></span>

### <span data-ttu-id="1605d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="1605d-132">System.String</span></span>

### <span data-ttu-id="1605d-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1605d-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1605d-134">출력</span><span class="sxs-lookup"><span data-stu-id="1605d-134">OUTPUTS</span></span>

### <span data-ttu-id="1605d-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="1605d-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="1605d-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1605d-136">NOTES</span></span>

## <span data-ttu-id="1605d-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1605d-137">RELATED LINKS</span></span>

[<span data-ttu-id="1605d-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="1605d-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="1605d-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="1605d-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="1605d-140">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="1605d-140">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


