---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmcustomscriptextension
schema: 2.0.0
ms.openlocfilehash: b6ce3afb8b280b9ca07746979f0bb5ba425afd82
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93883170"
---
# <span data-ttu-id="30623-101">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="30623-101">Get-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="30623-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30623-102">SYNOPSIS</span></span>
<span data-ttu-id="30623-103">사용자 지정 스크립트 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="30623-103">Gets information about a custom script extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30623-104">구문과</span><span class="sxs-lookup"><span data-stu-id="30623-104">SYNTAX</span></span>

```
Get-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30623-105">설명은</span><span class="sxs-lookup"><span data-stu-id="30623-105">DESCRIPTION</span></span>
<span data-ttu-id="30623-106">**AzureRmVMCustomScriptExtension** cmdlet은 가상 컴퓨터의 사용자 지정 스크립트 가상 컴퓨터 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="30623-106">The **Get-AzureRmVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="30623-107">예제의</span><span class="sxs-lookup"><span data-stu-id="30623-107">EXAMPLES</span></span>

### <span data-ttu-id="30623-108">예제 1: 사용자 지정 스크립트 확장 가져오기</span><span class="sxs-lookup"><span data-stu-id="30623-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="30623-109">이 명령은 VirtualMachine07 이라는 가상 컴퓨터에 대해 ContosoCustomScript 이라는 사용자 지정 스크립트 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="30623-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="30623-110">예제 2: 사용자 지정 스크립트 확장의 인스턴스 뷰 가져오기</span><span class="sxs-lookup"><span data-stu-id="30623-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="30623-111">이 명령은 VirtualMachine07 이라는 가상 컴퓨터에 대해 ContosoCustomScript 이라는 사용자 지정 스크립트 확장의 인스턴스 뷰를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="30623-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="30623-112">변수</span><span class="sxs-lookup"><span data-stu-id="30623-112">PARAMETERS</span></span>

### <span data-ttu-id="30623-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30623-113">-DefaultProfile</span></span>
<span data-ttu-id="30623-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="30623-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30623-115">-이름</span><span class="sxs-lookup"><span data-stu-id="30623-115">-Name</span></span>
<span data-ttu-id="30623-116">이 cmdlet에 대 한 정보를 가져오는 사용자 지정 스크립트 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30623-116">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30623-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30623-117">-ResourceGroupName</span></span>
<span data-ttu-id="30623-118">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30623-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="30623-119">-상태</span><span class="sxs-lookup"><span data-stu-id="30623-119">-Status</span></span>
<span data-ttu-id="30623-120">이 cmdlet이 사용자 지정 스크립트 확장의 인스턴스 뷰를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="30623-120">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30623-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="30623-121">-VMName</span></span>
<span data-ttu-id="30623-122">이 cmdlet이 사용자 지정 스크립트 확장을 가져오는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30623-122">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30623-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30623-123">CommonParameters</span></span>
<span data-ttu-id="30623-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="30623-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30623-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30623-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30623-126">입력</span><span class="sxs-lookup"><span data-stu-id="30623-126">INPUTS</span></span>

### <span data-ttu-id="30623-127">않아야</span><span class="sxs-lookup"><span data-stu-id="30623-127">None</span></span>
<span data-ttu-id="30623-128">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30623-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="30623-129">출력</span><span class="sxs-lookup"><span data-stu-id="30623-129">OUTPUTS</span></span>

### <span data-ttu-id="30623-130">VirtualMachineCustomScriptExtensionContext를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="30623-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span></span>

## <span data-ttu-id="30623-131">상속자</span><span class="sxs-lookup"><span data-stu-id="30623-131">NOTES</span></span>

## <span data-ttu-id="30623-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30623-132">RELATED LINKS</span></span>

[<span data-ttu-id="30623-133">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="30623-133">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="30623-134">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="30623-134">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="30623-135">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="30623-135">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


