---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
ms.openlocfilehash: ba4ac8d48c72ffac164e447777670c48f529f68f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328999"
---
# <span data-ttu-id="66f15-101">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="66f15-101">Get-AzVMDscExtension</span></span>

## <span data-ttu-id="66f15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66f15-102">SYNOPSIS</span></span>
<span data-ttu-id="66f15-103">특정 가상 머신에서 DSC 확장의 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="66f15-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

## <span data-ttu-id="66f15-104">구문</span><span class="sxs-lookup"><span data-stu-id="66f15-104">SYNTAX</span></span>

```
Get-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66f15-105">설명</span><span class="sxs-lookup"><span data-stu-id="66f15-105">DESCRIPTION</span></span>
<span data-ttu-id="66f15-106">**Get-AzVMDscExtension** cmdlet은 특정 가상 머신에서 DSC(Desired State Configuration) 확장의 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="66f15-106">The **Get-AzVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="66f15-107">예제</span><span class="sxs-lookup"><span data-stu-id="66f15-107">EXAMPLES</span></span>

### <span data-ttu-id="66f15-108">예제 1: DSC 확장의 설정 얻기</span><span class="sxs-lookup"><span data-stu-id="66f15-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="66f15-109">이 명령은 VM07이라는 가상 머신에서 DSC라는 확장의 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="66f15-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="66f15-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66f15-110">PARAMETERS</span></span>

### <span data-ttu-id="66f15-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66f15-111">-DefaultProfile</span></span>
<span data-ttu-id="66f15-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="66f15-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66f15-113">-Name</span><span class="sxs-lookup"><span data-stu-id="66f15-113">-Name</span></span>
<span data-ttu-id="66f15-114">확장을 나타내는 Azure Resource Manager 리소스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66f15-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="66f15-115">Set-AzVMDscExtension cmdlet은 이 이름을 **Get-AzVMDscExtension에서** 사용하는 동일한 값인 Microsoft.Powershell.DSC로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="66f15-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtension**.</span></span>
<span data-ttu-id="66f15-116">**Set-AzVMDscExtension** cmdlet에서 기본 이름을 변경하거나 Resource Manager 템플릿에서 다른 리소스 이름을 사용한 경우 이 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66f15-116">Specify this parameter only if you changed the default name in the **Set-AzVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66f15-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66f15-117">-ResourceGroupName</span></span>
<span data-ttu-id="66f15-118">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66f15-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="66f15-119">-Status</span><span class="sxs-lookup"><span data-stu-id="66f15-119">-Status</span></span>
<span data-ttu-id="66f15-120">이 cmdlet이 DSC 확장의 인스턴스 보기를 얻게 됐습니다.</span><span class="sxs-lookup"><span data-stu-id="66f15-120">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66f15-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="66f15-121">-VMName</span></span>
<span data-ttu-id="66f15-122">이 cmdlet이 DSC 확장을 받을 가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66f15-122">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

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

### <span data-ttu-id="66f15-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66f15-123">CommonParameters</span></span>
<span data-ttu-id="66f15-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="66f15-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66f15-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="66f15-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66f15-126">입력</span><span class="sxs-lookup"><span data-stu-id="66f15-126">INPUTS</span></span>

### <span data-ttu-id="66f15-127">System.String</span><span class="sxs-lookup"><span data-stu-id="66f15-127">System.String</span></span>

### <span data-ttu-id="66f15-128">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="66f15-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="66f15-129">출력</span><span class="sxs-lookup"><span data-stu-id="66f15-129">OUTPUTS</span></span>

### <span data-ttu-id="66f15-130">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="66f15-130">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="66f15-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="66f15-131">NOTES</span></span>

## <span data-ttu-id="66f15-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="66f15-132">RELATED LINKS</span></span>

[<span data-ttu-id="66f15-133">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="66f15-133">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="66f15-134">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="66f15-134">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


