---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMChefExtension.md
ms.openlocfilehash: 29d30bc039f826f4c2d56fde15286695187aabb5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533396"
---
# <span data-ttu-id="d347d-101">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="d347d-101">Get-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="d347d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d347d-102">SYNOPSIS</span></span>
<span data-ttu-id="d347d-103">요리사 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d347d-103">Gets information about a Chef extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d347d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d347d-104">SYNTAX</span></span>

### <span data-ttu-id="d347d-105">Linux</span><span class="sxs-lookup"><span data-stu-id="d347d-105">Linux</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Linux] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d347d-106">창을</span><span class="sxs-lookup"><span data-stu-id="d347d-106">Windows</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Windows] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d347d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d347d-107">DESCRIPTION</span></span>
<span data-ttu-id="d347d-108">**AzureVMChefExtension** cmdlet은 가상 컴퓨터에 설치 된 요리사 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d347d-108">The **Get-AzureVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="d347d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d347d-109">EXAMPLES</span></span>

### <span data-ttu-id="d347d-110">예제 1: Windows 가상 컴퓨터의 요리사 확장에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="d347d-110">Example 1: Get the details of Chef extension for a Windows virtual machine</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="d347d-111">이 명령은 ResourceGroup001 이라는 리소스 그룹에 속하는 Windows 가상 컴퓨터 WindowsVM001에서 요리사 확장명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d347d-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="d347d-112">예제 2: Linux 가상 컴퓨터의 요리사 확장에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="d347d-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="d347d-113">이 명령은 ResourceGroup002 이라는 리소스 그룹에 속하는 Linux 가상 컴퓨터 LinuxVM001에서 요리사 확장명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d347d-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="d347d-114">변수</span><span class="sxs-lookup"><span data-stu-id="d347d-114">PARAMETERS</span></span>

### <span data-ttu-id="d347d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d347d-115">-DefaultProfile</span></span>
<span data-ttu-id="d347d-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d347d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d347d-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="d347d-117">-Linux</span></span>
<span data-ttu-id="d347d-118">이 cmdlet이 Linux 가상 컴퓨터에서 작동 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d347d-118">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d347d-119">-이름</span><span class="sxs-lookup"><span data-stu-id="d347d-119">-Name</span></span>
<span data-ttu-id="d347d-120">요리사 확장명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d347d-120">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="d347d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d347d-121">-ResourceGroupName</span></span>
<span data-ttu-id="d347d-122">가상 컴퓨터를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d347d-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="d347d-123">-상태</span><span class="sxs-lookup"><span data-stu-id="d347d-123">-Status</span></span>
<span data-ttu-id="d347d-124">이 cmdlet이 요리사 extension의 instance 뷰에서만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d347d-124">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

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

### <span data-ttu-id="d347d-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="d347d-125">-VMName</span></span>
<span data-ttu-id="d347d-126">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d347d-126">Specifies the name of a virtual machine.</span></span>

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

### <span data-ttu-id="d347d-127">-Windows</span><span class="sxs-lookup"><span data-stu-id="d347d-127">-Windows</span></span>
<span data-ttu-id="d347d-128">이 cmdlet이 Windows 가상 컴퓨터에 대해 표시 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d347d-128">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d347d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d347d-129">CommonParameters</span></span>
<span data-ttu-id="d347d-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d347d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d347d-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d347d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d347d-132">입력</span><span class="sxs-lookup"><span data-stu-id="d347d-132">INPUTS</span></span>

### <span data-ttu-id="d347d-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d347d-133">System.String</span></span>

### <span data-ttu-id="d347d-134">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d347d-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d347d-135">출력</span><span class="sxs-lookup"><span data-stu-id="d347d-135">OUTPUTS</span></span>

### <span data-ttu-id="d347d-136">Microsoft. a. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="d347d-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="d347d-137">상속자</span><span class="sxs-lookup"><span data-stu-id="d347d-137">NOTES</span></span>

## <span data-ttu-id="d347d-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d347d-138">RELATED LINKS</span></span>

[<span data-ttu-id="d347d-139">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="d347d-139">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)

[<span data-ttu-id="d347d-140">제거-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="d347d-140">Remove-AzureRmVMChefExtension</span></span>](./Remove-AzureRmVMChefExtension.md)


