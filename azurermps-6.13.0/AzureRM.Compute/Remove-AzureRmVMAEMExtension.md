---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
ms.openlocfilehash: 96f9a3195747aff8d31261b7a6ae992a00adb82b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526248"
---
# <span data-ttu-id="df1c6-101">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="df1c6-101">Remove-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="df1c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df1c6-102">SYNOPSIS</span></span>
<span data-ttu-id="df1c6-103">가상 머신에서 AEM 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="df1c6-103">Removes the AEM extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df1c6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="df1c6-104">SYNTAX</span></span>

```
Remove-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df1c6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="df1c6-105">DESCRIPTION</span></span>
<span data-ttu-id="df1c6-106">**AzureRmVMAEMExtension** cmdlet은 가상 머신에서 Azure 확장 모니터링 (AEM) 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="df1c6-106">The **Remove-AzureRmVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="df1c6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="df1c6-107">EXAMPLES</span></span>

### <span data-ttu-id="df1c6-108">예제 1: AEM 확장 제거</span><span class="sxs-lookup"><span data-stu-id="df1c6-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="df1c6-109">이 명령은 contoso-server 라는 가상 컴퓨터에 대 한 AEM 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="df1c6-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="df1c6-110">변수</span><span class="sxs-lookup"><span data-stu-id="df1c6-110">PARAMETERS</span></span>

### <span data-ttu-id="df1c6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df1c6-111">-DefaultProfile</span></span>
<span data-ttu-id="df1c6-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="df1c6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df1c6-113">-이름</span><span class="sxs-lookup"><span data-stu-id="df1c6-113">-Name</span></span>
<span data-ttu-id="df1c6-114">이 cmdlet이 AEM 확장명을 제거 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="df1c6-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="df1c6-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="df1c6-115">-OSType</span></span>
<span data-ttu-id="df1c6-116">운영 체제 디스크의 운영 체제 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="df1c6-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="df1c6-117">운영 체제 디스크에 형식이 없는 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="df1c6-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="df1c6-118">이 매개 변수에 허용 되는 값은 Windows 및 Linux입니다.</span><span class="sxs-lookup"><span data-stu-id="df1c6-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="df1c6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df1c6-119">-ResourceGroupName</span></span>
<span data-ttu-id="df1c6-120">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="df1c6-120">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="df1c6-121">이 cmdlet은 해당 가상 컴퓨터에서 AEM 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="df1c6-121">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="df1c6-122">-VMName</span><span class="sxs-lookup"><span data-stu-id="df1c6-122">-VMName</span></span>
<span data-ttu-id="df1c6-123">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="df1c6-123">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="df1c6-124">이 cmdlet은이 매개 변수에서 지정 하는 가상 컴퓨터에 대 한 AEM 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="df1c6-124">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="df1c6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df1c6-125">CommonParameters</span></span>
<span data-ttu-id="df1c6-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="df1c6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df1c6-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df1c6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df1c6-128">입력</span><span class="sxs-lookup"><span data-stu-id="df1c6-128">INPUTS</span></span>

### <span data-ttu-id="df1c6-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="df1c6-129">System.String</span></span>

## <span data-ttu-id="df1c6-130">출력</span><span class="sxs-lookup"><span data-stu-id="df1c6-130">OUTPUTS</span></span>

### <span data-ttu-id="df1c6-131">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="df1c6-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="df1c6-132">상속자</span><span class="sxs-lookup"><span data-stu-id="df1c6-132">NOTES</span></span>

## <span data-ttu-id="df1c6-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="df1c6-133">RELATED LINKS</span></span>

[<span data-ttu-id="df1c6-134">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="df1c6-134">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="df1c6-135">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="df1c6-135">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="df1c6-136">테스트-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="df1c6-136">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


