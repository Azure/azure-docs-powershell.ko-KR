---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
ms.openlocfilehash: dc2e22acf8efd18a565c1ede7ff22aeb21679a47
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529899"
---
# <span data-ttu-id="60224-101">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="60224-101">Remove-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="60224-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60224-102">SYNOPSIS</span></span>
<span data-ttu-id="60224-103">가상 머신에서 요리사 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="60224-103">Removes the Chef extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60224-104">구문과</span><span class="sxs-lookup"><span data-stu-id="60224-104">SYNTAX</span></span>

### <span data-ttu-id="60224-105">Linux</span><span class="sxs-lookup"><span data-stu-id="60224-105">Linux</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60224-106">창을</span><span class="sxs-lookup"><span data-stu-id="60224-106">Windows</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60224-107">설명은</span><span class="sxs-lookup"><span data-stu-id="60224-107">DESCRIPTION</span></span>
<span data-ttu-id="60224-108">**AzureVMChefExtension** cmdlet는 가상 머신에서 요리사 extension을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="60224-108">The **Remove-AzureVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="60224-109">예제의</span><span class="sxs-lookup"><span data-stu-id="60224-109">EXAMPLES</span></span>

### <span data-ttu-id="60224-110">예제 1: Windows 가상 머신에서 요리사 확장 제거</span><span class="sxs-lookup"><span data-stu-id="60224-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="60224-111">이 명령은 ResourceGroup001 이라는 리소스 그룹에 속하는 Windows 기반 가상 컴퓨터 WindowsVM001에서 요리사 확장명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="60224-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="60224-112">예제 2: Linux 가상 머신에서 요리사 확장 제거</span><span class="sxs-lookup"><span data-stu-id="60224-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="60224-113">이 명령은 ResourceGroup002 이라는 리소스 그룹에 속하는 Linux 기반 가상 컴퓨터 LinuxVM001에서 요리사 확장명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="60224-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="60224-114">변수</span><span class="sxs-lookup"><span data-stu-id="60224-114">PARAMETERS</span></span>

### <span data-ttu-id="60224-115">-Linux</span><span class="sxs-lookup"><span data-stu-id="60224-115">-Linux</span></span>
<span data-ttu-id="60224-116">이 cmdlet이 Linux 가상 컴퓨터를 대상으로 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="60224-116">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

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

### <span data-ttu-id="60224-117">-이름</span><span class="sxs-lookup"><span data-stu-id="60224-117">-Name</span></span>
<span data-ttu-id="60224-118">이 cmdlet이 제거 하는 요리사 확장명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60224-118">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="60224-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60224-119">-ResourceGroupName</span></span>
<span data-ttu-id="60224-120">가상 컴퓨터를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60224-120">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="60224-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="60224-121">-VMName</span></span>
<span data-ttu-id="60224-122">이 cmdlet이 요리사 확장을 제거 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60224-122">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="60224-123">-Windows</span><span class="sxs-lookup"><span data-stu-id="60224-123">-Windows</span></span>
<span data-ttu-id="60224-124">이 cmdlet이 Windows 가상 컴퓨터를 대상으로 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="60224-124">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

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

### <span data-ttu-id="60224-125">-확인</span><span class="sxs-lookup"><span data-stu-id="60224-125">-Confirm</span></span>
<span data-ttu-id="60224-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="60224-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60224-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60224-127">-WhatIf</span></span>
<span data-ttu-id="60224-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="60224-128">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="60224-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60224-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60224-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60224-130">CommonParameters</span></span>
<span data-ttu-id="60224-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="60224-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60224-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60224-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60224-133">입력</span><span class="sxs-lookup"><span data-stu-id="60224-133">INPUTS</span></span>

### <span data-ttu-id="60224-134">않아야</span><span class="sxs-lookup"><span data-stu-id="60224-134">None</span></span>
<span data-ttu-id="60224-135">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60224-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="60224-136">출력</span><span class="sxs-lookup"><span data-stu-id="60224-136">OUTPUTS</span></span>

## <span data-ttu-id="60224-137">상속자</span><span class="sxs-lookup"><span data-stu-id="60224-137">NOTES</span></span>

## <span data-ttu-id="60224-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60224-138">RELATED LINKS</span></span>

[<span data-ttu-id="60224-139">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="60224-139">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="60224-140">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="60224-140">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)
