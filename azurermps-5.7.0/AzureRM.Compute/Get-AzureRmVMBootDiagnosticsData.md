---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMBootDiagnosticsData.md
ms.openlocfilehash: 5ae237c21c78f206188f23153bdf35c6bea10b19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702386"
---
# <span data-ttu-id="c9efa-101">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="c9efa-101">Get-AzureRmVMBootDiagnosticsData</span></span>

## <span data-ttu-id="c9efa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9efa-102">SYNOPSIS</span></span>
<span data-ttu-id="c9efa-103">가상 컴퓨터에 대 한 부팅 진단 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c9efa-103">Gets boot diagnostics data for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9efa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c9efa-104">SYNTAX</span></span>

### <span data-ttu-id="c9efa-105">WindowsParamSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c9efa-105">WindowsParamSet (Default)</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows]
 [-LocalPath] <String> [<CommonParameters>]
```

### <span data-ttu-id="c9efa-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="c9efa-106">LinuxParamSet</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux]
 [[-LocalPath] <String>] [<CommonParameters>]
```

## <span data-ttu-id="c9efa-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c9efa-107">DESCRIPTION</span></span>
<span data-ttu-id="c9efa-108">**AzureRmVMBootDiagnosticsData** cmdlet은 가상 컴퓨터에 대 한 부팅 진단 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c9efa-108">The **Get-AzureRmVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="c9efa-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c9efa-109">EXAMPLES</span></span>

### <span data-ttu-id="c9efa-110">예제 1: 부팅 진단 데이터 가져오기</span><span class="sxs-lookup"><span data-stu-id="c9efa-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzureRmVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="c9efa-111">이 명령은 ContosoVM07 이라는 가상 컴퓨터에 대 한 부팅 진단 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c9efa-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="c9efa-112">이 가상 컴퓨터는 Windows 운영 체제를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9efa-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="c9efa-113">명령은 지정 된 로컬 경로에 데이터를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9efa-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="c9efa-114">변수</span><span class="sxs-lookup"><span data-stu-id="c9efa-114">PARAMETERS</span></span>

### <span data-ttu-id="c9efa-115">-Linux</span><span class="sxs-lookup"><span data-stu-id="c9efa-115">-Linux</span></span>
<span data-ttu-id="c9efa-116">가상 컴퓨터가 Linux 운영 체제를 실행 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c9efa-116">Indicates that the virtual machine runs the Linux operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LinuxParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9efa-117">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="c9efa-117">-LocalPath</span></span>
<span data-ttu-id="c9efa-118">부팅 진단 데이터의 로컬 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9efa-118">Specifies the local path for the boot diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: WindowsParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: LinuxParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9efa-119">-이름</span><span class="sxs-lookup"><span data-stu-id="c9efa-119">-Name</span></span>
<span data-ttu-id="c9efa-120">이 cmdlet이 진단 데이터를 가져오는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9efa-120">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9efa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9efa-121">-ResourceGroupName</span></span>
<span data-ttu-id="c9efa-122">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9efa-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c9efa-123">-Windows</span><span class="sxs-lookup"><span data-stu-id="c9efa-123">-Windows</span></span>
<span data-ttu-id="c9efa-124">가상 컴퓨터가 Windows 운영 체제를 실행 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c9efa-124">Indicates that the virtual machine runs the Windows operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9efa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9efa-125">CommonParameters</span></span>
<span data-ttu-id="c9efa-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9efa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9efa-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9efa-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9efa-128">입력</span><span class="sxs-lookup"><span data-stu-id="c9efa-128">INPUTS</span></span>

### <span data-ttu-id="c9efa-129">않아야</span><span class="sxs-lookup"><span data-stu-id="c9efa-129">None</span></span>
<span data-ttu-id="c9efa-130">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9efa-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c9efa-131">출력</span><span class="sxs-lookup"><span data-stu-id="c9efa-131">OUTPUTS</span></span>

## <span data-ttu-id="c9efa-132">상속자</span><span class="sxs-lookup"><span data-stu-id="c9efa-132">NOTES</span></span>

## <span data-ttu-id="c9efa-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9efa-133">RELATED LINKS</span></span>

[<span data-ttu-id="c9efa-134">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="c9efa-134">Set-AzureRmVMBootDiagnostics</span></span>](./Set-AzureRmVMBootDiagnostics.md)


