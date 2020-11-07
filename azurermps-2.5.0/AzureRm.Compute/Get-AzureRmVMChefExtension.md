---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmchefextension
schema: 2.0.0
ms.openlocfilehash: e9047b681e669975e7113eb3970b2ee6573a68d5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881125"
---
# <span data-ttu-id="f3434-101">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="f3434-101">Get-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="f3434-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3434-102">SYNOPSIS</span></span>
<span data-ttu-id="f3434-103">요리사 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f3434-103">Gets information about a Chef extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3434-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f3434-104">SYNTAX</span></span>

### <span data-ttu-id="f3434-105">Linux</span><span class="sxs-lookup"><span data-stu-id="f3434-105">Linux</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Linux] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3434-106">창을</span><span class="sxs-lookup"><span data-stu-id="f3434-106">Windows</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Windows] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3434-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f3434-107">DESCRIPTION</span></span>
<span data-ttu-id="f3434-108">**AzureVMChefExtension** cmdlet은 가상 컴퓨터에 설치 된 요리사 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f3434-108">The **Get-AzureVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="f3434-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f3434-109">EXAMPLES</span></span>

### <span data-ttu-id="f3434-110">예제 1: Windows 가상 컴퓨터의 요리사 확장에 대 한 세부 정보 가져오기-</span><span class="sxs-lookup"><span data-stu-id="f3434-110">Example 1: Get the details of Chef extension for a Windows virtual machine-</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="f3434-111">이 명령은 ResourceGroup001 이라는 리소스 그룹에 속하는 Windows 가상 컴퓨터 WindowsVM001에서 요리사 확장명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f3434-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="f3434-112">예제 2: Linux 가상 컴퓨터의 요리사 확장에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="f3434-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="f3434-113">이 명령은 ResourceGroup002 이라는 리소스 그룹에 속하는 Linux 가상 컴퓨터 LinuxVM001에서 요리사 확장명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f3434-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="f3434-114">변수</span><span class="sxs-lookup"><span data-stu-id="f3434-114">PARAMETERS</span></span>

### <span data-ttu-id="f3434-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3434-115">-DefaultProfile</span></span>
<span data-ttu-id="f3434-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f3434-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3434-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="f3434-117">-Linux</span></span>
<span data-ttu-id="f3434-118">이 cmdlet이 Linux 가상 컴퓨터에서 작동 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f3434-118">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3434-119">-이름</span><span class="sxs-lookup"><span data-stu-id="f3434-119">-Name</span></span>
<span data-ttu-id="f3434-120">요리사 확장명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3434-120">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="f3434-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3434-121">-ResourceGroupName</span></span>
<span data-ttu-id="f3434-122">가상 컴퓨터를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3434-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="f3434-123">-상태</span><span class="sxs-lookup"><span data-stu-id="f3434-123">-Status</span></span>
<span data-ttu-id="f3434-124">이 cmdlet이 요리사 extension의 instance 뷰에서만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f3434-124">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

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

### <span data-ttu-id="f3434-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="f3434-125">-VMName</span></span>
<span data-ttu-id="f3434-126">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3434-126">Specifies the name of a virtual machine.</span></span>

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

### <span data-ttu-id="f3434-127">-Windows</span><span class="sxs-lookup"><span data-stu-id="f3434-127">-Windows</span></span>
<span data-ttu-id="f3434-128">이 cmdlet이 Windows 가상 컴퓨터에 대해 표시 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f3434-128">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3434-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3434-129">CommonParameters</span></span>
<span data-ttu-id="f3434-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3434-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3434-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3434-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3434-132">입력</span><span class="sxs-lookup"><span data-stu-id="f3434-132">INPUTS</span></span>

### <span data-ttu-id="f3434-133">않아야</span><span class="sxs-lookup"><span data-stu-id="f3434-133">None</span></span>
<span data-ttu-id="f3434-134">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f3434-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f3434-135">출력</span><span class="sxs-lookup"><span data-stu-id="f3434-135">OUTPUTS</span></span>

### <span data-ttu-id="f3434-136">Microsoft. a. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="f3434-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="f3434-137">상속자</span><span class="sxs-lookup"><span data-stu-id="f3434-137">NOTES</span></span>

## <span data-ttu-id="f3434-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3434-138">RELATED LINKS</span></span>

[<span data-ttu-id="f3434-139">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="f3434-139">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)

[<span data-ttu-id="f3434-140">제거-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="f3434-140">Remove-AzureRmVMChefExtension</span></span>](./Remove-AzureRmVMChefExtension.md)


