---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
ms.openlocfilehash: 1d1ccb7f8e47ce34b798124d54fdd85aa18c7d69
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94045053"
---
# <span data-ttu-id="70e18-101">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="70e18-101">Get-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="70e18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70e18-102">SYNOPSIS</span></span>
<span data-ttu-id="70e18-103">사용자 지정 스크립트 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70e18-103">Gets information about a custom script extension.</span></span>

## <span data-ttu-id="70e18-104">구문과</span><span class="sxs-lookup"><span data-stu-id="70e18-104">SYNTAX</span></span>

```
Get-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70e18-105">설명은</span><span class="sxs-lookup"><span data-stu-id="70e18-105">DESCRIPTION</span></span>
<span data-ttu-id="70e18-106">**AzVMCustomScriptExtension** cmdlet은 가상 컴퓨터의 사용자 지정 스크립트 가상 컴퓨터 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70e18-106">The **Get-AzVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="70e18-107">예제의</span><span class="sxs-lookup"><span data-stu-id="70e18-107">EXAMPLES</span></span>

### <span data-ttu-id="70e18-108">예제 1: 사용자 지정 스크립트 확장 가져오기</span><span class="sxs-lookup"><span data-stu-id="70e18-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="70e18-109">이 명령은 VirtualMachine07 이라는 가상 컴퓨터에 대해 ContosoCustomScript 이라는 사용자 지정 스크립트 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70e18-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="70e18-110">예제 2: 사용자 지정 스크립트 확장의 인스턴스 뷰 가져오기</span><span class="sxs-lookup"><span data-stu-id="70e18-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="70e18-111">이 명령은 VirtualMachine07 이라는 가상 컴퓨터에 대해 ContosoCustomScript 이라는 사용자 지정 스크립트 확장의 인스턴스 뷰를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70e18-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="70e18-112">변수</span><span class="sxs-lookup"><span data-stu-id="70e18-112">PARAMETERS</span></span>

### <span data-ttu-id="70e18-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70e18-113">-DefaultProfile</span></span>
<span data-ttu-id="70e18-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="70e18-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70e18-115">-이름</span><span class="sxs-lookup"><span data-stu-id="70e18-115">-Name</span></span>
<span data-ttu-id="70e18-116">이 cmdlet에 대 한 정보를 가져오는 사용자 지정 스크립트 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70e18-116">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70e18-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70e18-117">-ResourceGroupName</span></span>
<span data-ttu-id="70e18-118">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70e18-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="70e18-119">-상태</span><span class="sxs-lookup"><span data-stu-id="70e18-119">-Status</span></span>
<span data-ttu-id="70e18-120">이 cmdlet이 사용자 지정 스크립트 확장의 인스턴스 뷰를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70e18-120">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="70e18-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="70e18-121">-VMName</span></span>
<span data-ttu-id="70e18-122">이 cmdlet이 사용자 지정 스크립트 확장을 가져오는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70e18-122">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="70e18-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70e18-123">CommonParameters</span></span>
<span data-ttu-id="70e18-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="70e18-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70e18-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="70e18-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70e18-126">입력</span><span class="sxs-lookup"><span data-stu-id="70e18-126">INPUTS</span></span>

### <span data-ttu-id="70e18-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="70e18-127">System.String</span></span>

### <span data-ttu-id="70e18-128">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="70e18-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="70e18-129">출력</span><span class="sxs-lookup"><span data-stu-id="70e18-129">OUTPUTS</span></span>

### <span data-ttu-id="70e18-130">VirtualMachineCustomScriptExtensionContext를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="70e18-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span></span>

## <span data-ttu-id="70e18-131">상속자</span><span class="sxs-lookup"><span data-stu-id="70e18-131">NOTES</span></span>

## <span data-ttu-id="70e18-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70e18-132">RELATED LINKS</span></span>

[<span data-ttu-id="70e18-133">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="70e18-133">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="70e18-134">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="70e18-134">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="70e18-135">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="70e18-135">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


