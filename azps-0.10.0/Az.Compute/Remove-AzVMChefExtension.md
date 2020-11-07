---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMChefExtension.md
ms.openlocfilehash: 595d439707c67363faa7a780f8980efa7a1f3065
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876960"
---
# <span data-ttu-id="c5804-101">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="c5804-101">Remove-AzVMChefExtension</span></span>

## <span data-ttu-id="c5804-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5804-102">SYNOPSIS</span></span>
<span data-ttu-id="c5804-103">가상 머신에서 요리사 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5804-103">Removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="c5804-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c5804-104">SYNTAX</span></span>

### <span data-ttu-id="c5804-105">Linux</span><span class="sxs-lookup"><span data-stu-id="c5804-105">Linux</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5804-106">창을</span><span class="sxs-lookup"><span data-stu-id="c5804-106">Windows</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5804-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c5804-107">DESCRIPTION</span></span>
<span data-ttu-id="c5804-108">**AzureVMChefExtension** cmdlet는 가상 머신에서 요리사 extension을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5804-108">The **Remove-AzureVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="c5804-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c5804-109">EXAMPLES</span></span>

### <span data-ttu-id="c5804-110">예제 1: Windows 가상 머신에서 요리사 확장 제거</span><span class="sxs-lookup"><span data-stu-id="c5804-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="c5804-111">이 명령은 ResourceGroup001 이라는 리소스 그룹에 속하는 Windows 기반 가상 컴퓨터 WindowsVM001에서 요리사 확장명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5804-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="c5804-112">예제 2: Linux 가상 머신에서 요리사 확장 제거</span><span class="sxs-lookup"><span data-stu-id="c5804-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="c5804-113">이 명령은 ResourceGroup002 이라는 리소스 그룹에 속하는 Linux 기반 가상 컴퓨터 LinuxVM001에서 요리사 확장명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5804-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="c5804-114">변수</span><span class="sxs-lookup"><span data-stu-id="c5804-114">PARAMETERS</span></span>

### <span data-ttu-id="c5804-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5804-115">-DefaultProfile</span></span>
<span data-ttu-id="c5804-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c5804-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5804-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="c5804-117">-Linux</span></span>
<span data-ttu-id="c5804-118">이 cmdlet이 Linux 가상 컴퓨터를 대상으로 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c5804-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

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

### <span data-ttu-id="c5804-119">-이름</span><span class="sxs-lookup"><span data-stu-id="c5804-119">-Name</span></span>
<span data-ttu-id="c5804-120">이 cmdlet이 제거 하는 요리사 확장명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5804-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c5804-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5804-121">-ResourceGroupName</span></span>
<span data-ttu-id="c5804-122">가상 컴퓨터를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5804-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="c5804-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="c5804-123">-VMName</span></span>
<span data-ttu-id="c5804-124">이 cmdlet이 요리사 확장을 제거 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5804-124">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="c5804-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="c5804-125">-Windows</span></span>
<span data-ttu-id="c5804-126">이 cmdlet이 Windows 가상 컴퓨터를 대상으로 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c5804-126">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

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

### <span data-ttu-id="c5804-127">-확인</span><span class="sxs-lookup"><span data-stu-id="c5804-127">-Confirm</span></span>
<span data-ttu-id="c5804-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5804-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5804-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5804-129">-WhatIf</span></span>
<span data-ttu-id="c5804-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c5804-130">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="c5804-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c5804-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5804-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5804-132">CommonParameters</span></span>
<span data-ttu-id="c5804-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5804-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5804-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5804-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5804-135">입력</span><span class="sxs-lookup"><span data-stu-id="c5804-135">INPUTS</span></span>

### <span data-ttu-id="c5804-136">않아야</span><span class="sxs-lookup"><span data-stu-id="c5804-136">None</span></span>
<span data-ttu-id="c5804-137">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c5804-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c5804-138">출력</span><span class="sxs-lookup"><span data-stu-id="c5804-138">OUTPUTS</span></span>

### <span data-ttu-id="c5804-139">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="c5804-139">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="c5804-140">상속자</span><span class="sxs-lookup"><span data-stu-id="c5804-140">NOTES</span></span>

## <span data-ttu-id="c5804-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5804-141">RELATED LINKS</span></span>

[<span data-ttu-id="c5804-142">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="c5804-142">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="c5804-143">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="c5804-143">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)
