---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
ms.openlocfilehash: 71fcf62049cfb15e830b4c8c5f311c042de55bb9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957563"
---
# <span data-ttu-id="5e42d-101">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="5e42d-101">Remove-AzVMAEMExtension</span></span>

## <span data-ttu-id="5e42d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e42d-102">SYNOPSIS</span></span>
<span data-ttu-id="5e42d-103">가상 머신에서 AEM 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5e42d-103">Removes the AEM extension from a virtual machine.</span></span>

## <span data-ttu-id="5e42d-104">구문</span><span class="sxs-lookup"><span data-stu-id="5e42d-104">SYNTAX</span></span>

```
Remove-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e42d-105">설명</span><span class="sxs-lookup"><span data-stu-id="5e42d-105">DESCRIPTION</span></span>
<span data-ttu-id="5e42d-106">**Remove-AzVMAEMExtension** cmdlet은 가상 머신에서 AEM(Azure Enhanced Monitoring) 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5e42d-106">The **Remove-AzVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="5e42d-107">예제</span><span class="sxs-lookup"><span data-stu-id="5e42d-107">EXAMPLES</span></span>

### <span data-ttu-id="5e42d-108">예제 1: AEM 확장 제거</span><span class="sxs-lookup"><span data-stu-id="5e42d-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="5e42d-109">이 명령은 contoso-server라는 가상 머신에 대한 AEM 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5e42d-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="5e42d-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5e42d-110">PARAMETERS</span></span>

### <span data-ttu-id="5e42d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e42d-111">-DefaultProfile</span></span>
<span data-ttu-id="5e42d-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5e42d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e42d-113">-Name</span><span class="sxs-lookup"><span data-stu-id="5e42d-113">-Name</span></span>
<span data-ttu-id="5e42d-114">이 cmdlet에서 AEM 확장을 제거하는 가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5e42d-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="5e42d-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5e42d-115">-NoWait</span></span>
<span data-ttu-id="5e42d-116">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5e42d-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="5e42d-117">작업이 성공적으로 완료된지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e42d-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e42d-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="5e42d-118">-OSType</span></span>
<span data-ttu-id="5e42d-119">운영 체제 디스크의 운영 체제 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5e42d-119">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="5e42d-120">운영 체제 디스크에 형식이 없는 경우 이 매개 변수를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e42d-120">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="5e42d-121">이 매개 변수에 대해 허용되는 값은 Windows 및 Linux입니다.</span><span class="sxs-lookup"><span data-stu-id="5e42d-121">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e42d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e42d-122">-ResourceGroupName</span></span>
<span data-ttu-id="5e42d-123">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5e42d-123">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="5e42d-124">이 cmdlet은 해당 가상 머신에서 AEM 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5e42d-124">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="5e42d-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="5e42d-125">-VMName</span></span>
<span data-ttu-id="5e42d-126">가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5e42d-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="5e42d-127">이 cmdlet은 이 매개 변수가 지정하는 가상 머신에 대한 AEM 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5e42d-127">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="5e42d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e42d-128">CommonParameters</span></span>
<span data-ttu-id="5e42d-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5e42d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e42d-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e42d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e42d-131">입력</span><span class="sxs-lookup"><span data-stu-id="5e42d-131">INPUTS</span></span>

### <span data-ttu-id="5e42d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5e42d-132">System.String</span></span>

## <span data-ttu-id="5e42d-133">출력</span><span class="sxs-lookup"><span data-stu-id="5e42d-133">OUTPUTS</span></span>

### <span data-ttu-id="5e42d-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5e42d-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="5e42d-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5e42d-135">NOTES</span></span>

## <span data-ttu-id="5e42d-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5e42d-136">RELATED LINKS</span></span>

[<span data-ttu-id="5e42d-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="5e42d-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="5e42d-138">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="5e42d-138">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="5e42d-139">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="5e42d-139">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


