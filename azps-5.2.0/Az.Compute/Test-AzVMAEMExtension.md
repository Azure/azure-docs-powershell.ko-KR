---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/test-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
ms.openlocfilehash: ffc22a8937e56537de167046f661ee4b5d262fed
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347169"
---
# <span data-ttu-id="d4c4a-101">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d4c4a-101">Test-AzVMAEMExtension</span></span>

## <span data-ttu-id="d4c4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4c4a-102">SYNOPSIS</span></span>
<span data-ttu-id="d4c4a-103">AEM 확장의 구성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="d4c4a-103">Checks the configuration of the AEM extension.</span></span>

## <span data-ttu-id="d4c4a-104">구문</span><span class="sxs-lookup"><span data-stu-id="d4c4a-104">SYNTAX</span></span>

```
Test-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4c4a-105">설명</span><span class="sxs-lookup"><span data-stu-id="d4c4a-105">DESCRIPTION</span></span>
<span data-ttu-id="d4c4a-106">**Test-AzVMAEMExtension** cmdlet은 Azure AEM(고급 모니터링) 확장의 구성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="d4c4a-106">The **Test-AzVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="d4c4a-107">AEM 확장은 성능 데이터를 수집합니다.</span><span class="sxs-lookup"><span data-stu-id="d4c4a-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="d4c4a-108">이 cmdlet은 성능 데이터를 사용할 수 있는지 여부를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="d4c4a-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="d4c4a-109">예제</span><span class="sxs-lookup"><span data-stu-id="d4c4a-109">EXAMPLES</span></span>

### <span data-ttu-id="d4c4a-110">예제 1: AEM 확장의 구성 확인</span><span class="sxs-lookup"><span data-stu-id="d4c4a-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="d4c4a-111">이 명령은 contoso-server라는 가상 머신에 대한 AEM 확장의 구성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="d4c4a-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="d4c4a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4c4a-112">PARAMETERS</span></span>

### <span data-ttu-id="d4c4a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4c4a-113">-DefaultProfile</span></span>
<span data-ttu-id="d4c4a-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d4c4a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4c4a-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="d4c4a-115">-OSType</span></span>
<span data-ttu-id="d4c4a-116">운영 체제 디스크의 운영 체제 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d4c4a-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="d4c4a-117">운영 체제 디스크에 형식이 없는 경우 이 매개 변수를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4c4a-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="d4c4a-118">이 매개 변수에 허용되는 값은 Windows 및 Linux입니다.</span><span class="sxs-lookup"><span data-stu-id="d4c4a-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4c4a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4c4a-119">-ResourceGroupName</span></span>
<span data-ttu-id="d4c4a-120">이 cmdlet이 검사하는 가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d4c4a-120">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="d4c4a-121">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="d4c4a-121">-SkipStorageCheck</span></span>
<span data-ttu-id="d4c4a-122">이 cmdlet이 저장소 구성의 확인을 건너뛰고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4c4a-122">Indicates that this cmdlet skips the check of storage configuration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4c4a-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="d4c4a-123">-VMName</span></span>
<span data-ttu-id="d4c4a-124">가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d4c4a-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="d4c4a-125">이 cmdlet은 이 매개 변수가 지정하는 가상 머신에 대한 AEM 확장을 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="d4c4a-125">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="d4c4a-126">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="d4c4a-126">-WaitTimeInMinutes</span></span>
<span data-ttu-id="d4c4a-127">저장소 구성 검사에 대한 시간(분)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d4c4a-127">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4c4a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4c4a-128">CommonParameters</span></span>
<span data-ttu-id="d4c4a-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d4c4a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4c4a-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d4c4a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4c4a-131">입력</span><span class="sxs-lookup"><span data-stu-id="d4c4a-131">INPUTS</span></span>

### <span data-ttu-id="d4c4a-132">System.String</span><span class="sxs-lookup"><span data-stu-id="d4c4a-132">System.String</span></span>

## <span data-ttu-id="d4c4a-133">출력</span><span class="sxs-lookup"><span data-stu-id="d4c4a-133">OUTPUTS</span></span>

### <span data-ttu-id="d4c4a-134">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span><span class="sxs-lookup"><span data-stu-id="d4c4a-134">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span></span>

## <span data-ttu-id="d4c4a-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d4c4a-135">NOTES</span></span>

## <span data-ttu-id="d4c4a-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d4c4a-136">RELATED LINKS</span></span>

[<span data-ttu-id="d4c4a-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d4c4a-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="d4c4a-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d4c4a-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="d4c4a-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d4c4a-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)


