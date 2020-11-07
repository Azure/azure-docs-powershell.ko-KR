---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdiagnosticsextension
schema: 2.0.0
ms.openlocfilehash: e02c86407326d9ea5b12a5a589e5860c9dfb5c19
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93883178"
---
# <span data-ttu-id="34e40-101">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="34e40-101">Get-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="34e40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34e40-102">SYNOPSIS</span></span>
<span data-ttu-id="34e40-103">가상 컴퓨터의 진단 확장 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="34e40-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34e40-104">구문과</span><span class="sxs-lookup"><span data-stu-id="34e40-104">SYNTAX</span></span>

```
Get-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34e40-105">설명은</span><span class="sxs-lookup"><span data-stu-id="34e40-105">DESCRIPTION</span></span>
<span data-ttu-id="34e40-106">**AzureRmVMDiagnosticsExtension** cmdlet은 가상 컴퓨터에서 Azure Diagnostics 확장의 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="34e40-106">The **Get-AzureRmVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="34e40-107">예제의</span><span class="sxs-lookup"><span data-stu-id="34e40-107">EXAMPLES</span></span>

### <span data-ttu-id="34e40-108">예제 1: 가상 컴퓨터에 적용 되는 진단 확장 기능 가져오기</span><span class="sxs-lookup"><span data-stu-id="34e40-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="34e40-109">이 명령은 ContosoVM22 이라는 가상 컴퓨터에 적용 되는 진단 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="34e40-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="34e40-110">변수</span><span class="sxs-lookup"><span data-stu-id="34e40-110">PARAMETERS</span></span>

### <span data-ttu-id="34e40-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34e40-111">-DefaultProfile</span></span>
<span data-ttu-id="34e40-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="34e40-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34e40-113">-이름</span><span class="sxs-lookup"><span data-stu-id="34e40-113">-Name</span></span>
<span data-ttu-id="34e40-114">이 cmdlet에 대 한 설정을 가져오는 진단 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34e40-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34e40-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34e40-115">-ResourceGroupName</span></span>
<span data-ttu-id="34e40-116">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34e40-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="34e40-117">-상태</span><span class="sxs-lookup"><span data-stu-id="34e40-117">-Status</span></span>
<span data-ttu-id="34e40-118">이 cmdlet이 상태 값을 사용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="34e40-118">Indicates that this cmdlet uses the Status value.</span></span>

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

### <span data-ttu-id="34e40-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="34e40-119">-VMName</span></span>
<span data-ttu-id="34e40-120">이 cmdlet이 진단 확장을 가져오는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34e40-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="34e40-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34e40-121">CommonParameters</span></span>
<span data-ttu-id="34e40-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="34e40-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34e40-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34e40-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34e40-124">입력</span><span class="sxs-lookup"><span data-stu-id="34e40-124">INPUTS</span></span>

### <span data-ttu-id="34e40-125">않아야</span><span class="sxs-lookup"><span data-stu-id="34e40-125">None</span></span>
<span data-ttu-id="34e40-126">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34e40-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="34e40-127">출력</span><span class="sxs-lookup"><span data-stu-id="34e40-127">OUTPUTS</span></span>

### <span data-ttu-id="34e40-128">Microsoft. a. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="34e40-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="34e40-129">상속자</span><span class="sxs-lookup"><span data-stu-id="34e40-129">NOTES</span></span>

## <span data-ttu-id="34e40-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="34e40-130">RELATED LINKS</span></span>

[<span data-ttu-id="34e40-131">제거-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="34e40-131">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="34e40-132">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="34e40-132">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)


