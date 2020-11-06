---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
ms.openlocfilehash: fb31bffbdb61c42ea1388c85b71f26af69056c54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529902"
---
# <span data-ttu-id="f49f0-101">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f49f0-101">Remove-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="f49f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f49f0-102">SYNOPSIS</span></span>
<span data-ttu-id="f49f0-103">가상 머신에서 AEM 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49f0-103">Removes the AEM extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f49f0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f49f0-104">SYNTAX</span></span>

```
Remove-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [<CommonParameters>]
```

## <span data-ttu-id="f49f0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f49f0-105">DESCRIPTION</span></span>
<span data-ttu-id="f49f0-106">**AzureRmVMAEMExtension** cmdlet은 가상 머신에서 Azure 확장 모니터링 (AEM) 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49f0-106">The **Remove-AzureRmVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="f49f0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f49f0-107">EXAMPLES</span></span>

### <span data-ttu-id="f49f0-108">예제 1: AEM 확장 제거</span><span class="sxs-lookup"><span data-stu-id="f49f0-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="f49f0-109">이 명령은 contoso-server 라는 가상 컴퓨터에 대 한 AEM 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49f0-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="f49f0-110">변수</span><span class="sxs-lookup"><span data-stu-id="f49f0-110">PARAMETERS</span></span>

### <span data-ttu-id="f49f0-111">-이름</span><span class="sxs-lookup"><span data-stu-id="f49f0-111">-Name</span></span>
<span data-ttu-id="f49f0-112">이 cmdlet이 AEM 확장명을 제거 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49f0-112">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="f49f0-113">-OSType</span><span class="sxs-lookup"><span data-stu-id="f49f0-113">-OSType</span></span>
<span data-ttu-id="f49f0-114">운영 체제 디스크의 운영 체제 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49f0-114">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="f49f0-115">운영 체제 디스크에 형식이 없는 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49f0-115">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="f49f0-116">이 매개 변수에 허용 되는 값은 Windows 및 Linux입니다.</span><span class="sxs-lookup"><span data-stu-id="f49f0-116">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f49f0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f49f0-117">-ResourceGroupName</span></span>
<span data-ttu-id="f49f0-118">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49f0-118">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="f49f0-119">이 cmdlet은 해당 가상 컴퓨터에서 AEM 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49f0-119">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="f49f0-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="f49f0-120">-VMName</span></span>
<span data-ttu-id="f49f0-121">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49f0-121">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="f49f0-122">이 cmdlet은이 매개 변수에서 지정 하는 가상 컴퓨터에 대 한 AEM 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49f0-122">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="f49f0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f49f0-123">CommonParameters</span></span>
<span data-ttu-id="f49f0-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49f0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f49f0-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f49f0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f49f0-126">입력</span><span class="sxs-lookup"><span data-stu-id="f49f0-126">INPUTS</span></span>

### <span data-ttu-id="f49f0-127">않아야</span><span class="sxs-lookup"><span data-stu-id="f49f0-127">None</span></span>
<span data-ttu-id="f49f0-128">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f49f0-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f49f0-129">출력</span><span class="sxs-lookup"><span data-stu-id="f49f0-129">OUTPUTS</span></span>

## <span data-ttu-id="f49f0-130">상속자</span><span class="sxs-lookup"><span data-stu-id="f49f0-130">NOTES</span></span>

## <span data-ttu-id="f49f0-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f49f0-131">RELATED LINKS</span></span>

[<span data-ttu-id="f49f0-132">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f49f0-132">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="f49f0-133">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f49f0-133">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="f49f0-134">테스트-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f49f0-134">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


