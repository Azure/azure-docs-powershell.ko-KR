---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
ms.openlocfilehash: 052082672dd822b78ff6c47abf7710c87c35a746
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868958"
---
# <span data-ttu-id="7d014-101">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="7d014-101">Remove-AzVMChefExtension</span></span>

## <span data-ttu-id="7d014-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d014-102">SYNOPSIS</span></span>
<span data-ttu-id="7d014-103">가상 머신에서 요리사 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d014-103">Removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="7d014-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7d014-104">SYNTAX</span></span>

### <span data-ttu-id="7d014-105">Linux</span><span class="sxs-lookup"><span data-stu-id="7d014-105">Linux</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d014-106">창을</span><span class="sxs-lookup"><span data-stu-id="7d014-106">Windows</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d014-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7d014-107">DESCRIPTION</span></span>
<span data-ttu-id="7d014-108">**AzVMChefExtension** cmdlet는 가상 머신에서 요리사 extension을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d014-108">The **Remove-AzVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="7d014-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7d014-109">EXAMPLES</span></span>

### <span data-ttu-id="7d014-110">예제 1: Windows 가상 머신에서 요리사 확장 제거</span><span class="sxs-lookup"><span data-stu-id="7d014-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="7d014-111">이 명령은 ResourceGroup001 이라는 리소스 그룹에 속하는 Windows 기반 가상 컴퓨터 WindowsVM001에서 요리사 확장명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d014-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="7d014-112">예제 2: Linux 가상 머신에서 요리사 확장 제거</span><span class="sxs-lookup"><span data-stu-id="7d014-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="7d014-113">이 명령은 ResourceGroup002 이라는 리소스 그룹에 속하는 Linux 기반 가상 컴퓨터 LinuxVM001에서 요리사 확장명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d014-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="7d014-114">변수</span><span class="sxs-lookup"><span data-stu-id="7d014-114">PARAMETERS</span></span>

### <span data-ttu-id="7d014-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d014-115">-DefaultProfile</span></span>
<span data-ttu-id="7d014-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7d014-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d014-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="7d014-117">-Linux</span></span>
<span data-ttu-id="7d014-118">이 cmdlet이 Linux 가상 컴퓨터를 대상으로 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7d014-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

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

### <span data-ttu-id="7d014-119">-이름</span><span class="sxs-lookup"><span data-stu-id="7d014-119">-Name</span></span>
<span data-ttu-id="7d014-120">이 cmdlet이 제거 하는 요리사 확장명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d014-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7d014-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d014-121">-ResourceGroupName</span></span>
<span data-ttu-id="7d014-122">가상 컴퓨터를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d014-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="7d014-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="7d014-123">-VMName</span></span>
<span data-ttu-id="7d014-124">이 cmdlet이 요리사 확장을 제거 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d014-124">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="7d014-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="7d014-125">-Windows</span></span>
<span data-ttu-id="7d014-126">이 cmdlet이 Windows 가상 컴퓨터를 대상으로 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7d014-126">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

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

### <span data-ttu-id="7d014-127">-확인</span><span class="sxs-lookup"><span data-stu-id="7d014-127">-Confirm</span></span>
<span data-ttu-id="7d014-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d014-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d014-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d014-129">-WhatIf</span></span>
<span data-ttu-id="7d014-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7d014-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d014-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d014-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d014-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d014-132">CommonParameters</span></span>
<span data-ttu-id="7d014-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d014-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d014-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d014-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d014-135">입력</span><span class="sxs-lookup"><span data-stu-id="7d014-135">INPUTS</span></span>

### <span data-ttu-id="7d014-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7d014-136">System.String</span></span>

## <span data-ttu-id="7d014-137">출력</span><span class="sxs-lookup"><span data-stu-id="7d014-137">OUTPUTS</span></span>

### <span data-ttu-id="7d014-138">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="7d014-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="7d014-139">상속자</span><span class="sxs-lookup"><span data-stu-id="7d014-139">NOTES</span></span>

## <span data-ttu-id="7d014-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d014-140">RELATED LINKS</span></span>

[<span data-ttu-id="7d014-141">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="7d014-141">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="7d014-142">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="7d014-142">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)
