---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
ms.openlocfilehash: da19894751c7b653dbc70d606a44464973d9b38c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536719"
---
# <span data-ttu-id="0f571-101">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="0f571-101">Remove-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="0f571-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f571-102">SYNOPSIS</span></span>
<span data-ttu-id="0f571-103">가상 머신에서 요리사 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f571-103">Removes the Chef extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f571-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0f571-104">SYNTAX</span></span>

### <span data-ttu-id="0f571-105">Linux</span><span class="sxs-lookup"><span data-stu-id="0f571-105">Linux</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f571-106">창을</span><span class="sxs-lookup"><span data-stu-id="0f571-106">Windows</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f571-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0f571-107">DESCRIPTION</span></span>
<span data-ttu-id="0f571-108">**AzureVMChefExtension** cmdlet는 가상 머신에서 요리사 extension을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f571-108">The **Remove-AzureVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="0f571-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0f571-109">EXAMPLES</span></span>

### <span data-ttu-id="0f571-110">예제 1: Windows 가상 머신에서 요리사 확장 제거</span><span class="sxs-lookup"><span data-stu-id="0f571-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="0f571-111">이 명령은 ResourceGroup001 이라는 리소스 그룹에 속하는 Windows 기반 가상 컴퓨터 WindowsVM001에서 요리사 확장명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f571-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="0f571-112">예제 2: Linux 가상 머신에서 요리사 확장 제거</span><span class="sxs-lookup"><span data-stu-id="0f571-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="0f571-113">이 명령은 ResourceGroup002 이라는 리소스 그룹에 속하는 Linux 기반 가상 컴퓨터 LinuxVM001에서 요리사 확장명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f571-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="0f571-114">변수</span><span class="sxs-lookup"><span data-stu-id="0f571-114">PARAMETERS</span></span>

### <span data-ttu-id="0f571-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f571-115">-DefaultProfile</span></span>
<span data-ttu-id="0f571-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0f571-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f571-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="0f571-117">-Linux</span></span>
<span data-ttu-id="0f571-118">이 cmdlet이 Linux 가상 컴퓨터를 대상으로 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0f571-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

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

### <span data-ttu-id="0f571-119">-이름</span><span class="sxs-lookup"><span data-stu-id="0f571-119">-Name</span></span>
<span data-ttu-id="0f571-120">이 cmdlet이 제거 하는 요리사 확장명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f571-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0f571-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f571-121">-ResourceGroupName</span></span>
<span data-ttu-id="0f571-122">가상 컴퓨터를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f571-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="0f571-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="0f571-123">-VMName</span></span>
<span data-ttu-id="0f571-124">이 cmdlet이 요리사 확장을 제거 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f571-124">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="0f571-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="0f571-125">-Windows</span></span>
<span data-ttu-id="0f571-126">이 cmdlet이 Windows 가상 컴퓨터를 대상으로 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0f571-126">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

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

### <span data-ttu-id="0f571-127">-확인</span><span class="sxs-lookup"><span data-stu-id="0f571-127">-Confirm</span></span>
<span data-ttu-id="0f571-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f571-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f571-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f571-129">-WhatIf</span></span>
<span data-ttu-id="0f571-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0f571-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f571-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0f571-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f571-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f571-132">CommonParameters</span></span>
<span data-ttu-id="0f571-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f571-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f571-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f571-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f571-135">입력</span><span class="sxs-lookup"><span data-stu-id="0f571-135">INPUTS</span></span>

### <span data-ttu-id="0f571-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0f571-136">System.String</span></span>

## <span data-ttu-id="0f571-137">출력</span><span class="sxs-lookup"><span data-stu-id="0f571-137">OUTPUTS</span></span>

### <span data-ttu-id="0f571-138">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="0f571-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0f571-139">상속자</span><span class="sxs-lookup"><span data-stu-id="0f571-139">NOTES</span></span>

## <span data-ttu-id="0f571-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0f571-140">RELATED LINKS</span></span>

[<span data-ttu-id="0f571-141">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="0f571-141">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="0f571-142">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="0f571-142">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)
