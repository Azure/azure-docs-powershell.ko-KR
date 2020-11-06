---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
ms.openlocfilehash: d766102b0e87968e59bdd9bf63157dd62e977a25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525263"
---
# <span data-ttu-id="f0b53-101">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f0b53-101">Test-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="f0b53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0b53-102">SYNOPSIS</span></span>
<span data-ttu-id="f0b53-103">AEM 확장의 구성을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b53-103">Checks the configuration of the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0b53-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f0b53-104">SYNTAX</span></span>

```
Test-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [<CommonParameters>]
```

## <span data-ttu-id="f0b53-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f0b53-105">DESCRIPTION</span></span>
<span data-ttu-id="f0b53-106">**AzureRmVMAEMExtension** Cmdlet은 Azure 개선 모니터링 (AEM) 확장의 구성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b53-106">The **Test-AzureRmVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="f0b53-107">AEM 확장은 성능 데이터를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b53-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="f0b53-108">이 cmdlet은 성능 데이터를 사용할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b53-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="f0b53-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f0b53-109">EXAMPLES</span></span>

### <span data-ttu-id="f0b53-110">예제 1: AEM 확장의 구성 확인</span><span class="sxs-lookup"><span data-stu-id="f0b53-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="f0b53-111">이 명령은 contoso-server 라는 가상 컴퓨터에 대 한 AEM 확장의 구성을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b53-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="f0b53-112">변수</span><span class="sxs-lookup"><span data-stu-id="f0b53-112">PARAMETERS</span></span>

### <span data-ttu-id="f0b53-113">-OSType</span><span class="sxs-lookup"><span data-stu-id="f0b53-113">-OSType</span></span>
<span data-ttu-id="f0b53-114">운영 체제 디스크의 운영 체제 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b53-114">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="f0b53-115">운영 체제 디스크에 형식이 없는 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b53-115">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="f0b53-116">이 매개 변수에 허용 되는 값은 Windows 및 Linux입니다.</span><span class="sxs-lookup"><span data-stu-id="f0b53-116">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0b53-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0b53-117">-ResourceGroupName</span></span>
<span data-ttu-id="f0b53-118">이 cmdlet이 확인 하는 가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b53-118">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="f0b53-119">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="f0b53-119">-SkipStorageCheck</span></span>
<span data-ttu-id="f0b53-120">이 cmdlet이 저장소 구성 검사를 생략 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f0b53-120">Indicates that this cmdlet skips the check of storage configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0b53-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="f0b53-121">-VMName</span></span>
<span data-ttu-id="f0b53-122">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b53-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="f0b53-123">이 cmdlet은이 매개 변수에서 지정 하는 가상 컴퓨터에 대 한 AEM 확장을 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b53-123">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="f0b53-124">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="f0b53-124">-WaitTimeInMinutes</span></span>
<span data-ttu-id="f0b53-125">저장소 구성 검사에 대 한 시간 초과 기간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b53-125">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0b53-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0b53-126">CommonParameters</span></span>
<span data-ttu-id="f0b53-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b53-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0b53-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0b53-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0b53-129">입력</span><span class="sxs-lookup"><span data-stu-id="f0b53-129">INPUTS</span></span>

### <span data-ttu-id="f0b53-130">않아야</span><span class="sxs-lookup"><span data-stu-id="f0b53-130">None</span></span>
<span data-ttu-id="f0b53-131">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0b53-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f0b53-132">출력</span><span class="sxs-lookup"><span data-stu-id="f0b53-132">OUTPUTS</span></span>

## <span data-ttu-id="f0b53-133">상속자</span><span class="sxs-lookup"><span data-stu-id="f0b53-133">NOTES</span></span>

## <span data-ttu-id="f0b53-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f0b53-134">RELATED LINKS</span></span>

[<span data-ttu-id="f0b53-135">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f0b53-135">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="f0b53-136">제거-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f0b53-136">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="f0b53-137">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f0b53-137">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)


