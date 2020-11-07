---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMConfig.md
ms.openlocfilehash: 45cb93e652f9c1524ef1bb11972f184336ef7328
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702752"
---
# <span data-ttu-id="8b146-101">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="8b146-101">New-AzureRmVMConfig</span></span>

## <span data-ttu-id="8b146-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b146-102">SYNOPSIS</span></span>
<span data-ttu-id="8b146-103">구성할 수 있는 가상 컴퓨터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8b146-103">Creates a configurable virtual machine object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b146-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8b146-104">SYNTAX</span></span>

```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [-LicenseType <String>] [-IdentityType <ResourceIdentityType>] [-Tags <Hashtable>] [<CommonParameters>]
```

## <span data-ttu-id="8b146-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8b146-105">DESCRIPTION</span></span>
<span data-ttu-id="8b146-106">**AzureRmVMConfig** Cmdlet은 Azure에 대해 구성할 수 있는 로컬 가상 컴퓨터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8b146-106">The **New-AzureRmVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="8b146-107">다른 cmdlet을 사용 하 여 AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, Set-AzureRmVMOSDisk 등의 가상 컴퓨터 개체를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b146-107">Other cmdlets can be used to configure a virtual machine object, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="8b146-108">예제의</span><span class="sxs-lookup"><span data-stu-id="8b146-108">EXAMPLES</span></span>

### <span data-ttu-id="8b146-109">예제 1: 가상 컴퓨터 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="8b146-109">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="8b146-110">첫 번째 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailablitySet03 이라는 가용성 집합을 가져온 다음 해당 개체를 $AvailabilitySet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b146-110">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="8b146-111">두 번째 명령은 가상 컴퓨터 개체를 만든 다음 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b146-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="8b146-112">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b146-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="8b146-113">가상 머신이 $AvailabilitySet에 저장 된 가용성 집합에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="8b146-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="8b146-114">변수</span><span class="sxs-lookup"><span data-stu-id="8b146-114">PARAMETERS</span></span>

### <span data-ttu-id="8b146-115">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="8b146-115">-AvailabilitySetId</span></span>
<span data-ttu-id="8b146-116">가용성 집합의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b146-116">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="8b146-117">가용성 집합 개체를 가져오려면 Get-AzureRmAvailabilitySet cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b146-117">To obtain an availability set object, use the Get-AzureRmAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="8b146-118">가용성 집합 개체에 ID 속성이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b146-118">The availability set object contains an ID property.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b146-119">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="8b146-119">-IdentityType</span></span>
<span data-ttu-id="8b146-120">가상 컴퓨터의 id입니다 (구성 된 경우).</span><span class="sxs-lookup"><span data-stu-id="8b146-120">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b146-121">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="8b146-121">-LicenseType</span></span>
<span data-ttu-id="8b146-122">라이선스 형식-고유한 라이선스 시나리오를 가져오는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8b146-122">The license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b146-123">태그</span><span class="sxs-lookup"><span data-stu-id="8b146-123">-Tags</span></span>
<span data-ttu-id="8b146-124">리소스에 연결 된 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="8b146-124">The tags attached to the resource.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b146-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="8b146-125">-VMName</span></span>
<span data-ttu-id="8b146-126">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b146-126">Specifies a name for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b146-127">-VMSize</span><span class="sxs-lookup"><span data-stu-id="8b146-127">-VMSize</span></span>
<span data-ttu-id="8b146-128">가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b146-128">Specifies the size for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b146-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b146-129">CommonParameters</span></span>
<span data-ttu-id="8b146-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b146-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b146-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b146-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b146-132">입력</span><span class="sxs-lookup"><span data-stu-id="8b146-132">INPUTS</span></span>

### <span data-ttu-id="8b146-133">않아야</span><span class="sxs-lookup"><span data-stu-id="8b146-133">None</span></span>
<span data-ttu-id="8b146-134">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8b146-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8b146-135">출력</span><span class="sxs-lookup"><span data-stu-id="8b146-135">OUTPUTS</span></span>

## <span data-ttu-id="8b146-136">상속자</span><span class="sxs-lookup"><span data-stu-id="8b146-136">NOTES</span></span>

## <span data-ttu-id="8b146-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b146-137">RELATED LINKS</span></span>

[<span data-ttu-id="8b146-138">업데이트-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8b146-138">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="8b146-139">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="8b146-139">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="8b146-140">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="8b146-140">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="8b146-141">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8b146-141">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)


