---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/test-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
ms.openlocfilehash: 7fe1219e9124a63784f3d064ffb25ed9d8271356
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697172"
---
# <span data-ttu-id="adb58-101">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="adb58-101">Test-AzVMAEMExtension</span></span>

## <span data-ttu-id="adb58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adb58-102">SYNOPSIS</span></span>
<span data-ttu-id="adb58-103">AEM 확장의 구성을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb58-103">Checks the configuration of the AEM extension.</span></span>

## <span data-ttu-id="adb58-104">구문과</span><span class="sxs-lookup"><span data-stu-id="adb58-104">SYNTAX</span></span>

```
Test-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="adb58-105">설명은</span><span class="sxs-lookup"><span data-stu-id="adb58-105">DESCRIPTION</span></span>
<span data-ttu-id="adb58-106">**AzVMAEMExtension** Cmdlet은 Azure 개선 모니터링 (AEM) 확장의 구성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb58-106">The **Test-AzVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="adb58-107">AEM 확장은 성능 데이터를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb58-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="adb58-108">이 cmdlet은 성능 데이터를 사용할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb58-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="adb58-109">예제의</span><span class="sxs-lookup"><span data-stu-id="adb58-109">EXAMPLES</span></span>

### <span data-ttu-id="adb58-110">예제 1: AEM 확장의 구성 확인</span><span class="sxs-lookup"><span data-stu-id="adb58-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="adb58-111">이 명령은 contoso-server 라는 가상 컴퓨터에 대 한 AEM 확장의 구성을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb58-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="adb58-112">변수</span><span class="sxs-lookup"><span data-stu-id="adb58-112">PARAMETERS</span></span>

### <span data-ttu-id="adb58-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adb58-113">-DefaultProfile</span></span>
<span data-ttu-id="adb58-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="adb58-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="adb58-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="adb58-115">-OSType</span></span>
<span data-ttu-id="adb58-116">운영 체제 디스크의 운영 체제 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb58-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="adb58-117">운영 체제 디스크에 형식이 없는 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb58-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="adb58-118">이 매개 변수에 허용 되는 값은 Windows 및 Linux입니다.</span><span class="sxs-lookup"><span data-stu-id="adb58-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="adb58-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adb58-119">-ResourceGroupName</span></span>
<span data-ttu-id="adb58-120">이 cmdlet이 확인 하는 가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb58-120">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="adb58-121">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="adb58-121">-SkipStorageCheck</span></span>
<span data-ttu-id="adb58-122">이 cmdlet이 저장소 구성 검사를 생략 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="adb58-122">Indicates that this cmdlet skips the check of storage configuration.</span></span>

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

### <span data-ttu-id="adb58-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="adb58-123">-VMName</span></span>
<span data-ttu-id="adb58-124">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb58-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="adb58-125">이 cmdlet은이 매개 변수에서 지정 하는 가상 컴퓨터에 대 한 AEM 확장을 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb58-125">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="adb58-126">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="adb58-126">-WaitTimeInMinutes</span></span>
<span data-ttu-id="adb58-127">저장소 구성 검사에 대 한 시간 초과 기간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb58-127">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

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

### <span data-ttu-id="adb58-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adb58-128">CommonParameters</span></span>
<span data-ttu-id="adb58-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb58-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adb58-130">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="adb58-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adb58-131">입력</span><span class="sxs-lookup"><span data-stu-id="adb58-131">INPUTS</span></span>

### <span data-ttu-id="adb58-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="adb58-132">System.String</span></span>

## <span data-ttu-id="adb58-133">출력</span><span class="sxs-lookup"><span data-stu-id="adb58-133">OUTPUTS</span></span>

### <span data-ttu-id="adb58-134">AEM를 반환 합니다. AEMTestResult</span><span class="sxs-lookup"><span data-stu-id="adb58-134">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span></span>

## <span data-ttu-id="adb58-135">상속자</span><span class="sxs-lookup"><span data-stu-id="adb58-135">NOTES</span></span>

## <span data-ttu-id="adb58-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="adb58-136">RELATED LINKS</span></span>

[<span data-ttu-id="adb58-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="adb58-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="adb58-138">제거-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="adb58-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="adb58-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="adb58-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)


