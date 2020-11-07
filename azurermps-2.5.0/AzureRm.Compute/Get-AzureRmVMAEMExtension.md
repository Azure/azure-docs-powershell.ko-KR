---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaemextension
schema: 2.0.0
ms.openlocfilehash: f5936a4be0170279d7416b05dc2b61fd22cfcca5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881134"
---
# <span data-ttu-id="ffe21-101">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ffe21-101">Get-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="ffe21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffe21-102">SYNOPSIS</span></span>
<span data-ttu-id="ffe21-103">AEM 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ffe21-103">Gets information about the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffe21-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ffe21-104">SYNTAX</span></span>

```
Get-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffe21-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ffe21-105">DESCRIPTION</span></span>
<span data-ttu-id="ffe21-106">**AzureRmVMAEMExtension** CMDLET은 AEM (Azure 확장 모니터링) 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ffe21-106">The **Get-AzureRmVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="ffe21-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ffe21-107">EXAMPLES</span></span>

### <span data-ttu-id="ffe21-108">예제 1: AEM 확장명 가져오기</span><span class="sxs-lookup"><span data-stu-id="ffe21-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="ffe21-109">이 명령은 contoso-server 라는 가상 컴퓨터에 대 한 AEM 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ffe21-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="ffe21-110">변수</span><span class="sxs-lookup"><span data-stu-id="ffe21-110">PARAMETERS</span></span>

### <span data-ttu-id="ffe21-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffe21-111">-DefaultProfile</span></span>
<span data-ttu-id="ffe21-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ffe21-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffe21-113">-이름</span><span class="sxs-lookup"><span data-stu-id="ffe21-113">-Name</span></span>
<span data-ttu-id="ffe21-114">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffe21-114">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="ffe21-115">이 cmdlet은이 cmdlet에서 지정 하는 가상 컴퓨터의 AEM 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ffe21-115">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="ffe21-116">-OSType</span><span class="sxs-lookup"><span data-stu-id="ffe21-116">-OSType</span></span>
<span data-ttu-id="ffe21-117">운영 체제 디스크의 운영 체제 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffe21-117">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="ffe21-118">운영 체제 디스크에 형식이 없는 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffe21-118">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="ffe21-119">이 매개 변수에 허용 되는 값은 Windows 및 Linux입니다.</span><span class="sxs-lookup"><span data-stu-id="ffe21-119">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffe21-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffe21-120">-ResourceGroupName</span></span>
<span data-ttu-id="ffe21-121">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffe21-121">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="ffe21-122">이 cmdlet은 해당 가상 컴퓨터의 AEM 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ffe21-122">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="ffe21-123">-상태</span><span class="sxs-lookup"><span data-stu-id="ffe21-123">-Status</span></span>
<span data-ttu-id="ffe21-124">이 cmdlet이 AEM extension의 instance 뷰에서만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ffe21-124">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

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

### <span data-ttu-id="ffe21-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="ffe21-125">-VMName</span></span>
<span data-ttu-id="ffe21-126">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffe21-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="ffe21-127">이 cmdlet은이 매개 변수에서 지정 하는 가상 컴퓨터의 AEM extension에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ffe21-127">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="ffe21-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffe21-128">CommonParameters</span></span>
<span data-ttu-id="ffe21-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffe21-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffe21-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffe21-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffe21-131">입력</span><span class="sxs-lookup"><span data-stu-id="ffe21-131">INPUTS</span></span>

### <span data-ttu-id="ffe21-132">않아야</span><span class="sxs-lookup"><span data-stu-id="ffe21-132">None</span></span>
<span data-ttu-id="ffe21-133">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ffe21-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ffe21-134">출력</span><span class="sxs-lookup"><span data-stu-id="ffe21-134">OUTPUTS</span></span>

### <span data-ttu-id="ffe21-135">Microsoft. a. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="ffe21-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="ffe21-136">상속자</span><span class="sxs-lookup"><span data-stu-id="ffe21-136">NOTES</span></span>

## <span data-ttu-id="ffe21-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ffe21-137">RELATED LINKS</span></span>

[<span data-ttu-id="ffe21-138">제거-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ffe21-138">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="ffe21-139">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ffe21-139">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="ffe21-140">테스트-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ffe21-140">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


