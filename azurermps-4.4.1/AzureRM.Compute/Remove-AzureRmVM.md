---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVM.md
ms.openlocfilehash: 3cc48d103867008b247ce480de43d1ccadc68d18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533108"
---
# <span data-ttu-id="21ac6-101">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="21ac6-101">Remove-AzureRmVM</span></span>

## <span data-ttu-id="21ac6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21ac6-102">SYNOPSIS</span></span>
<span data-ttu-id="21ac6-103">Azure에서 가상 컴퓨터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ac6-103">Removes a virtual machine from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21ac6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="21ac6-104">SYNTAX</span></span>

### <span data-ttu-id="21ac6-105">ResourceGroupNameParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="21ac6-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21ac6-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="21ac6-106">IdParameterSetName</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21ac6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="21ac6-107">DESCRIPTION</span></span>
<span data-ttu-id="21ac6-108">**AzureRmVM** Cmdlet은 Azure에서 가상 컴퓨터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ac6-108">The **Remove-AzureRmVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="21ac6-109">예제의</span><span class="sxs-lookup"><span data-stu-id="21ac6-109">EXAMPLES</span></span>

### <span data-ttu-id="21ac6-110">예제 1: 가상 컴퓨터 제거</span><span class="sxs-lookup"><span data-stu-id="21ac6-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="21ac6-111">이 명령은 리소스 그룹 ResourceGroup11에서 VirtualMachine07 이라는 가상 컴퓨터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ac6-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="21ac6-112">변수</span><span class="sxs-lookup"><span data-stu-id="21ac6-112">PARAMETERS</span></span>

### <span data-ttu-id="21ac6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21ac6-113">-DefaultProfile</span></span>
<span data-ttu-id="21ac6-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="21ac6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21ac6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="21ac6-115">-Force</span></span>
<span data-ttu-id="21ac6-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ac6-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ac6-117">-Id</span><span class="sxs-lookup"><span data-stu-id="21ac6-117">-Id</span></span>
<span data-ttu-id="21ac6-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="21ac6-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21ac6-119">-이름</span><span class="sxs-lookup"><span data-stu-id="21ac6-119">-Name</span></span>
<span data-ttu-id="21ac6-120">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="21ac6-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21ac6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21ac6-121">-ResourceGroupName</span></span>
<span data-ttu-id="21ac6-122">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ac6-122">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21ac6-123">-확인</span><span class="sxs-lookup"><span data-stu-id="21ac6-123">-Confirm</span></span>
<span data-ttu-id="21ac6-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ac6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21ac6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21ac6-125">-WhatIf</span></span>
<span data-ttu-id="21ac6-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="21ac6-126">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="21ac6-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="21ac6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21ac6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21ac6-128">CommonParameters</span></span>
<span data-ttu-id="21ac6-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ac6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21ac6-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21ac6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21ac6-131">입력</span><span class="sxs-lookup"><span data-stu-id="21ac6-131">INPUTS</span></span>

## <span data-ttu-id="21ac6-132">출력</span><span class="sxs-lookup"><span data-stu-id="21ac6-132">OUTPUTS</span></span>

## <span data-ttu-id="21ac6-133">상속자</span><span class="sxs-lookup"><span data-stu-id="21ac6-133">NOTES</span></span>

## <span data-ttu-id="21ac6-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="21ac6-134">RELATED LINKS</span></span>

[<span data-ttu-id="21ac6-135">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="21ac6-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="21ac6-136">새로운 AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="21ac6-136">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="21ac6-137">다시 시작-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="21ac6-137">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="21ac6-138">시작-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="21ac6-138">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="21ac6-139">중지-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="21ac6-139">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="21ac6-140">업데이트-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="21ac6-140">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


