---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
ms.openlocfilehash: 224d11aba6eece63c7c080415253b4833c665cee
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876971"
---
# <span data-ttu-id="000a8-101">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="000a8-101">Remove-AzVMAEMExtension</span></span>

## <span data-ttu-id="000a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="000a8-102">SYNOPSIS</span></span>
<span data-ttu-id="000a8-103">가상 머신에서 AEM 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="000a8-103">Removes the AEM extension from a virtual machine.</span></span>

## <span data-ttu-id="000a8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="000a8-104">SYNTAX</span></span>

```
Remove-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="000a8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="000a8-105">DESCRIPTION</span></span>
<span data-ttu-id="000a8-106">**AzVMAEMExtension** cmdlet은 가상 머신에서 Azure 확장 모니터링 (AEM) 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="000a8-106">The **Remove-AzVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="000a8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="000a8-107">EXAMPLES</span></span>

### <span data-ttu-id="000a8-108">예제 1: AEM 확장 제거</span><span class="sxs-lookup"><span data-stu-id="000a8-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="000a8-109">이 명령은 contoso-server 라는 가상 컴퓨터에 대 한 AEM 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="000a8-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="000a8-110">변수</span><span class="sxs-lookup"><span data-stu-id="000a8-110">PARAMETERS</span></span>

### <span data-ttu-id="000a8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="000a8-111">-DefaultProfile</span></span>
<span data-ttu-id="000a8-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="000a8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="000a8-113">-이름</span><span class="sxs-lookup"><span data-stu-id="000a8-113">-Name</span></span>
<span data-ttu-id="000a8-114">이 cmdlet이 AEM 확장명을 제거 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="000a8-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="000a8-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="000a8-115">-OSType</span></span>
<span data-ttu-id="000a8-116">운영 체제 디스크의 운영 체제 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="000a8-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="000a8-117">운영 체제 디스크에 형식이 없는 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="000a8-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="000a8-118">이 매개 변수에 허용 되는 값은 Windows 및 Linux입니다.</span><span class="sxs-lookup"><span data-stu-id="000a8-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="000a8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="000a8-119">-ResourceGroupName</span></span>
<span data-ttu-id="000a8-120">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="000a8-120">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="000a8-121">이 cmdlet은 해당 가상 컴퓨터에서 AEM 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="000a8-121">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="000a8-122">-VMName</span><span class="sxs-lookup"><span data-stu-id="000a8-122">-VMName</span></span>
<span data-ttu-id="000a8-123">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="000a8-123">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="000a8-124">이 cmdlet은이 매개 변수에서 지정 하는 가상 컴퓨터에 대 한 AEM 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="000a8-124">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="000a8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="000a8-125">CommonParameters</span></span>
<span data-ttu-id="000a8-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="000a8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="000a8-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="000a8-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="000a8-128">입력</span><span class="sxs-lookup"><span data-stu-id="000a8-128">INPUTS</span></span>

### <span data-ttu-id="000a8-129">않아야</span><span class="sxs-lookup"><span data-stu-id="000a8-129">None</span></span>
<span data-ttu-id="000a8-130">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="000a8-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="000a8-131">출력</span><span class="sxs-lookup"><span data-stu-id="000a8-131">OUTPUTS</span></span>

### <span data-ttu-id="000a8-132">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="000a8-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="000a8-133">상속자</span><span class="sxs-lookup"><span data-stu-id="000a8-133">NOTES</span></span>

## <span data-ttu-id="000a8-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="000a8-134">RELATED LINKS</span></span>

[<span data-ttu-id="000a8-135">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="000a8-135">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="000a8-136">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="000a8-136">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="000a8-137">테스트-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="000a8-137">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


