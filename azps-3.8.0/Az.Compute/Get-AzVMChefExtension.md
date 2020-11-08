---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
ms.openlocfilehash: 02647fc2148069e2c408c979e4b258fd0a641fc0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94045055"
---
# <span data-ttu-id="7d4fe-101">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="7d4fe-101">Get-AzVMChefExtension</span></span>

## <span data-ttu-id="7d4fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d4fe-102">SYNOPSIS</span></span>
<span data-ttu-id="7d4fe-103">요리사 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7d4fe-103">Gets information about a Chef extension.</span></span>

## <span data-ttu-id="7d4fe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7d4fe-104">SYNTAX</span></span>

### <span data-ttu-id="7d4fe-105">Linux</span><span class="sxs-lookup"><span data-stu-id="7d4fe-105">Linux</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d4fe-106">창을</span><span class="sxs-lookup"><span data-stu-id="7d4fe-106">Windows</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d4fe-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7d4fe-107">DESCRIPTION</span></span>
<span data-ttu-id="7d4fe-108">**AzVMChefExtension** cmdlet은 가상 컴퓨터에 설치 된 요리사 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7d4fe-108">The **Get-AzVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="7d4fe-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7d4fe-109">EXAMPLES</span></span>

### <span data-ttu-id="7d4fe-110">예제 1: Windows 가상 컴퓨터의 요리사 확장에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="7d4fe-110">Example 1: Get the details of Chef extension for a Windows virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="7d4fe-111">이 명령은 ResourceGroup001 이라는 리소스 그룹에 속하는 Windows 가상 컴퓨터 WindowsVM001에서 요리사 확장명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7d4fe-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="7d4fe-112">예제 2: Linux 가상 컴퓨터의 요리사 확장에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="7d4fe-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="7d4fe-113">이 명령은 ResourceGroup002 이라는 리소스 그룹에 속하는 Linux 가상 컴퓨터 LinuxVM001에서 요리사 확장명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7d4fe-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="7d4fe-114">변수</span><span class="sxs-lookup"><span data-stu-id="7d4fe-114">PARAMETERS</span></span>

### <span data-ttu-id="7d4fe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d4fe-115">-DefaultProfile</span></span>
<span data-ttu-id="7d4fe-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7d4fe-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d4fe-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="7d4fe-117">-Linux</span></span>
<span data-ttu-id="7d4fe-118">이 cmdlet이 Linux 가상 컴퓨터에서 작동 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7d4fe-118">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

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

### <span data-ttu-id="7d4fe-119">-이름</span><span class="sxs-lookup"><span data-stu-id="7d4fe-119">-Name</span></span>
<span data-ttu-id="7d4fe-120">요리사 확장명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d4fe-120">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="7d4fe-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d4fe-121">-ResourceGroupName</span></span>
<span data-ttu-id="7d4fe-122">가상 컴퓨터를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d4fe-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="7d4fe-123">-상태</span><span class="sxs-lookup"><span data-stu-id="7d4fe-123">-Status</span></span>
<span data-ttu-id="7d4fe-124">이 cmdlet이 요리사 extension의 instance 뷰에서만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7d4fe-124">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

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

### <span data-ttu-id="7d4fe-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="7d4fe-125">-VMName</span></span>
<span data-ttu-id="7d4fe-126">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d4fe-126">Specifies the name of a virtual machine.</span></span>

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

### <span data-ttu-id="7d4fe-127">-Windows</span><span class="sxs-lookup"><span data-stu-id="7d4fe-127">-Windows</span></span>
<span data-ttu-id="7d4fe-128">이 cmdlet이 Windows 가상 컴퓨터에 대해 표시 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7d4fe-128">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

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

### <span data-ttu-id="7d4fe-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d4fe-129">CommonParameters</span></span>
<span data-ttu-id="7d4fe-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d4fe-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d4fe-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7d4fe-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d4fe-132">입력</span><span class="sxs-lookup"><span data-stu-id="7d4fe-132">INPUTS</span></span>

### <span data-ttu-id="7d4fe-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7d4fe-133">System.String</span></span>

### <span data-ttu-id="7d4fe-134">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="7d4fe-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7d4fe-135">출력</span><span class="sxs-lookup"><span data-stu-id="7d4fe-135">OUTPUTS</span></span>

### <span data-ttu-id="7d4fe-136">Microsoft. a. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="7d4fe-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="7d4fe-137">상속자</span><span class="sxs-lookup"><span data-stu-id="7d4fe-137">NOTES</span></span>

## <span data-ttu-id="7d4fe-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d4fe-138">RELATED LINKS</span></span>

[<span data-ttu-id="7d4fe-139">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="7d4fe-139">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)

[<span data-ttu-id="7d4fe-140">제거-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="7d4fe-140">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)


