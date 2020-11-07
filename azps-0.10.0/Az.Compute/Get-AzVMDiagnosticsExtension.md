---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 9137b62098a1441cea8acc53c52c0e0ea835ff09
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877072"
---
# <span data-ttu-id="0f955-101">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="0f955-101">Get-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="0f955-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f955-102">SYNOPSIS</span></span>
<span data-ttu-id="0f955-103">가상 컴퓨터의 진단 확장 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0f955-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="0f955-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0f955-104">SYNTAX</span></span>

```
Get-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f955-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0f955-105">DESCRIPTION</span></span>
<span data-ttu-id="0f955-106">**AzVMDiagnosticsExtension** cmdlet은 가상 컴퓨터에서 Azure Diagnostics 확장의 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0f955-106">The **Get-AzVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="0f955-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0f955-107">EXAMPLES</span></span>

### <span data-ttu-id="0f955-108">예제 1: 가상 컴퓨터에 적용 되는 진단 확장 기능 가져오기</span><span class="sxs-lookup"><span data-stu-id="0f955-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="0f955-109">이 명령은 ContosoVM22 이라는 가상 컴퓨터에 적용 되는 진단 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0f955-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="0f955-110">변수</span><span class="sxs-lookup"><span data-stu-id="0f955-110">PARAMETERS</span></span>

### <span data-ttu-id="0f955-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f955-111">-DefaultProfile</span></span>
<span data-ttu-id="0f955-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0f955-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f955-113">-이름</span><span class="sxs-lookup"><span data-stu-id="0f955-113">-Name</span></span>
<span data-ttu-id="0f955-114">이 cmdlet에 대 한 설정을 가져오는 진단 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f955-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

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

### <span data-ttu-id="0f955-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f955-115">-ResourceGroupName</span></span>
<span data-ttu-id="0f955-116">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f955-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0f955-117">-상태</span><span class="sxs-lookup"><span data-stu-id="0f955-117">-Status</span></span>
<span data-ttu-id="0f955-118">이 cmdlet이 상태 값을 사용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0f955-118">Indicates that this cmdlet uses the Status value.</span></span>

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

### <span data-ttu-id="0f955-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="0f955-119">-VMName</span></span>
<span data-ttu-id="0f955-120">이 cmdlet이 진단 확장을 가져오는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f955-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="0f955-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f955-121">CommonParameters</span></span>
<span data-ttu-id="0f955-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f955-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f955-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f955-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f955-124">입력</span><span class="sxs-lookup"><span data-stu-id="0f955-124">INPUTS</span></span>

### <span data-ttu-id="0f955-125">않아야</span><span class="sxs-lookup"><span data-stu-id="0f955-125">None</span></span>
<span data-ttu-id="0f955-126">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0f955-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0f955-127">출력</span><span class="sxs-lookup"><span data-stu-id="0f955-127">OUTPUTS</span></span>

### <span data-ttu-id="0f955-128">Microsoft. a. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="0f955-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="0f955-129">상속자</span><span class="sxs-lookup"><span data-stu-id="0f955-129">NOTES</span></span>

## <span data-ttu-id="0f955-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0f955-130">RELATED LINKS</span></span>

[<span data-ttu-id="0f955-131">제거-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="0f955-131">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="0f955-132">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="0f955-132">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)


