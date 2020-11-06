---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
ms.openlocfilehash: fbc357decbf4bdcd2e378294fed43125d38fd873
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528616"
---
# <span data-ttu-id="cbcf9-101">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="cbcf9-101">Get-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="cbcf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbcf9-102">SYNOPSIS</span></span>
<span data-ttu-id="cbcf9-103">가상 컴퓨터의 진단 확장 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cbcf9-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbcf9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cbcf9-104">SYNTAX</span></span>

```
Get-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbcf9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cbcf9-105">DESCRIPTION</span></span>
<span data-ttu-id="cbcf9-106">**AzureRmVMDiagnosticsExtension** cmdlet은 가상 컴퓨터에서 Azure Diagnostics 확장의 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cbcf9-106">The **Get-AzureRmVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="cbcf9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cbcf9-107">EXAMPLES</span></span>

### <span data-ttu-id="cbcf9-108">예제 1: 가상 컴퓨터에 적용 되는 진단 확장 기능 가져오기</span><span class="sxs-lookup"><span data-stu-id="cbcf9-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="cbcf9-109">이 명령은 ContosoVM22 이라는 가상 컴퓨터에 적용 되는 진단 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cbcf9-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="cbcf9-110">변수</span><span class="sxs-lookup"><span data-stu-id="cbcf9-110">PARAMETERS</span></span>

### <span data-ttu-id="cbcf9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbcf9-111">-DefaultProfile</span></span>
<span data-ttu-id="cbcf9-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cbcf9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbcf9-113">-이름</span><span class="sxs-lookup"><span data-stu-id="cbcf9-113">-Name</span></span>
<span data-ttu-id="cbcf9-114">이 cmdlet에 대 한 설정을 가져오는 진단 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbcf9-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

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

### <span data-ttu-id="cbcf9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbcf9-115">-ResourceGroupName</span></span>
<span data-ttu-id="cbcf9-116">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbcf9-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="cbcf9-117">-상태</span><span class="sxs-lookup"><span data-stu-id="cbcf9-117">-Status</span></span>
<span data-ttu-id="cbcf9-118">이 cmdlet이 상태 값을 사용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cbcf9-118">Indicates that this cmdlet uses the Status value.</span></span>

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

### <span data-ttu-id="cbcf9-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="cbcf9-119">-VMName</span></span>
<span data-ttu-id="cbcf9-120">이 cmdlet이 진단 확장을 가져오는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbcf9-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="cbcf9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbcf9-121">CommonParameters</span></span>
<span data-ttu-id="cbcf9-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbcf9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbcf9-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbcf9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbcf9-124">입력</span><span class="sxs-lookup"><span data-stu-id="cbcf9-124">INPUTS</span></span>

### <span data-ttu-id="cbcf9-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cbcf9-125">System.String</span></span>

### <span data-ttu-id="cbcf9-126">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="cbcf9-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cbcf9-127">출력</span><span class="sxs-lookup"><span data-stu-id="cbcf9-127">OUTPUTS</span></span>

### <span data-ttu-id="cbcf9-128">Microsoft. a. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="cbcf9-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="cbcf9-129">상속자</span><span class="sxs-lookup"><span data-stu-id="cbcf9-129">NOTES</span></span>

## <span data-ttu-id="cbcf9-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cbcf9-130">RELATED LINKS</span></span>

[<span data-ttu-id="cbcf9-131">제거-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="cbcf9-131">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="cbcf9-132">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="cbcf9-132">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)


