---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
ms.openlocfilehash: 3d4867e33fe388195904d31fa7e83abe26dde474
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528593"
---
# <span data-ttu-id="4553a-101">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4553a-101">Get-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="4553a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4553a-102">SYNOPSIS</span></span>
<span data-ttu-id="4553a-103">AEM 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4553a-103">Gets information about the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4553a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4553a-104">SYNTAX</span></span>

```
Get-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4553a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4553a-105">DESCRIPTION</span></span>
<span data-ttu-id="4553a-106">**AzureRmVMAEMExtension** CMDLET은 AEM (Azure 확장 모니터링) 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4553a-106">The **Get-AzureRmVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="4553a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4553a-107">EXAMPLES</span></span>

### <span data-ttu-id="4553a-108">예제 1: AEM 확장명 가져오기</span><span class="sxs-lookup"><span data-stu-id="4553a-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="4553a-109">이 명령은 contoso-server 라는 가상 컴퓨터에 대 한 AEM 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4553a-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="4553a-110">변수</span><span class="sxs-lookup"><span data-stu-id="4553a-110">PARAMETERS</span></span>

### <span data-ttu-id="4553a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4553a-111">-DefaultProfile</span></span>
<span data-ttu-id="4553a-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4553a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4553a-113">-이름</span><span class="sxs-lookup"><span data-stu-id="4553a-113">-Name</span></span>
<span data-ttu-id="4553a-114">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4553a-114">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="4553a-115">이 cmdlet은이 cmdlet에서 지정 하는 가상 컴퓨터의 AEM 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4553a-115">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="4553a-116">-OSType</span><span class="sxs-lookup"><span data-stu-id="4553a-116">-OSType</span></span>
<span data-ttu-id="4553a-117">운영 체제 디스크의 운영 체제 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4553a-117">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="4553a-118">운영 체제 디스크에 형식이 없는 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4553a-118">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="4553a-119">이 매개 변수에 허용 되는 값은 Windows 및 Linux입니다.</span><span class="sxs-lookup"><span data-stu-id="4553a-119">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4553a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4553a-120">-ResourceGroupName</span></span>
<span data-ttu-id="4553a-121">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4553a-121">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="4553a-122">이 cmdlet은 해당 가상 컴퓨터의 AEM 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4553a-122">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="4553a-123">-상태</span><span class="sxs-lookup"><span data-stu-id="4553a-123">-Status</span></span>
<span data-ttu-id="4553a-124">이 cmdlet이 AEM extension의 instance 뷰에서만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4553a-124">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4553a-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="4553a-125">-VMName</span></span>
<span data-ttu-id="4553a-126">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4553a-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="4553a-127">이 cmdlet은이 매개 변수에서 지정 하는 가상 컴퓨터의 AEM extension에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4553a-127">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="4553a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4553a-128">CommonParameters</span></span>
<span data-ttu-id="4553a-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4553a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4553a-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4553a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4553a-131">입력</span><span class="sxs-lookup"><span data-stu-id="4553a-131">INPUTS</span></span>

### <span data-ttu-id="4553a-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4553a-132">System.String</span></span>

### <span data-ttu-id="4553a-133">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4553a-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4553a-134">출력</span><span class="sxs-lookup"><span data-stu-id="4553a-134">OUTPUTS</span></span>

### <span data-ttu-id="4553a-135">Microsoft. a. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="4553a-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="4553a-136">상속자</span><span class="sxs-lookup"><span data-stu-id="4553a-136">NOTES</span></span>

## <span data-ttu-id="4553a-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4553a-137">RELATED LINKS</span></span>

[<span data-ttu-id="4553a-138">제거-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4553a-138">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="4553a-139">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4553a-139">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="4553a-140">테스트-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4553a-140">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


