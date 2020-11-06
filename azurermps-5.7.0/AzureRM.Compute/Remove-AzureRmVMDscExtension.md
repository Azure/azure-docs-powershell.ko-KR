---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDscExtension.md
ms.openlocfilehash: b3e9f8703b2130426d98a4a59fe25eb2f3f8fbdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525311"
---
# <span data-ttu-id="6f36a-101">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="6f36a-101">Remove-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="6f36a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f36a-102">SYNOPSIS</span></span>
<span data-ttu-id="6f36a-103">리소스 그룹의 가상 컴퓨터에서 DSC 확장 처리기를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f36a-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f36a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6f36a-104">SYNTAX</span></span>

```
Remove-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f36a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6f36a-105">DESCRIPTION</span></span>
<span data-ttu-id="6f36a-106">**AzureRmVMDscExtension** cmdlet은 리소스 그룹의 가상 컴퓨터에서 원하는 상태 구성 (DSC) 확장 처리기를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f36a-106">The **Remove-AzureRmVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="6f36a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6f36a-107">EXAMPLES</span></span>

### <span data-ttu-id="6f36a-108">예제 1: DSC 확장 제거</span><span class="sxs-lookup"><span data-stu-id="6f36a-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzureRmVMDscExtension -ResouceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="6f36a-109">이 명령은 VM07 이라는 가상 컴퓨터에서 DSC 라는 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f36a-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="6f36a-110">변수</span><span class="sxs-lookup"><span data-stu-id="6f36a-110">PARAMETERS</span></span>

### <span data-ttu-id="6f36a-111">-이름</span><span class="sxs-lookup"><span data-stu-id="6f36a-111">-Name</span></span>
<span data-ttu-id="6f36a-112">이 cmdlet이 제거 하는 DSC 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f36a-112">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="6f36a-113">Set-AzureRmVMDscExtension cmdlet은이 이름을 **AzureRmVMDscExtension** 에 사용 되는 기본 값인 Microsoft Powershell로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f36a-113">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzureRmVMDscExtension**.</span></span>

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

### <span data-ttu-id="6f36a-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f36a-114">-ResourceGroupName</span></span>
<span data-ttu-id="6f36a-115">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f36a-115">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="6f36a-116">-VMName</span><span class="sxs-lookup"><span data-stu-id="6f36a-116">-VMName</span></span>
<span data-ttu-id="6f36a-117">이 cmdlet이 DSC 확장을 제거 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f36a-117">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

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

### <span data-ttu-id="6f36a-118">-확인</span><span class="sxs-lookup"><span data-stu-id="6f36a-118">-Confirm</span></span>
<span data-ttu-id="6f36a-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f36a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f36a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f36a-120">-WhatIf</span></span>
<span data-ttu-id="6f36a-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6f36a-121">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="6f36a-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6f36a-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f36a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f36a-123">CommonParameters</span></span>
<span data-ttu-id="6f36a-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f36a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f36a-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f36a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f36a-126">입력</span><span class="sxs-lookup"><span data-stu-id="6f36a-126">INPUTS</span></span>

### <span data-ttu-id="6f36a-127">않아야</span><span class="sxs-lookup"><span data-stu-id="6f36a-127">None</span></span>
<span data-ttu-id="6f36a-128">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6f36a-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6f36a-129">출력</span><span class="sxs-lookup"><span data-stu-id="6f36a-129">OUTPUTS</span></span>

## <span data-ttu-id="6f36a-130">상속자</span><span class="sxs-lookup"><span data-stu-id="6f36a-130">NOTES</span></span>

## <span data-ttu-id="6f36a-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f36a-131">RELATED LINKS</span></span>

[<span data-ttu-id="6f36a-132">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="6f36a-132">Get-AzureRmVMDscExtension</span></span>](./Get-AzureRmVMDscExtension.md)

[<span data-ttu-id="6f36a-133">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="6f36a-133">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


