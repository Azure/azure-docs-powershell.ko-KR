---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzContainerService.md
ms.openlocfilehash: 1a0daa4bf336ba970c12c24db3d5aab73641aaea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877095"
---
# <span data-ttu-id="b0889-101">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="b0889-101">Get-AzContainerService</span></span>

## <span data-ttu-id="b0889-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0889-102">SYNOPSIS</span></span>
<span data-ttu-id="b0889-103">컨테이너 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b0889-103">Gets a container service.</span></span>

## <span data-ttu-id="b0889-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b0889-104">SYNTAX</span></span>

```
Get-AzContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0889-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b0889-105">DESCRIPTION</span></span>
<span data-ttu-id="b0889-106">**Get-AzContainerService** cmdlet은 컨테이너 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b0889-106">The **Get-AzContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="b0889-107">상태, 마스터 및 에이전트 수, 마스터 및 에이전트의 정규화 된 도메인 이름 등 컨테이너 서비스의 속성을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0889-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="b0889-108">예제의</span><span class="sxs-lookup"><span data-stu-id="b0889-108">EXAMPLES</span></span>

### <span data-ttu-id="b0889-109">예제 1: 컨테이너 서비스 가져오기</span><span class="sxs-lookup"><span data-stu-id="b0889-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="b0889-110">이 명령은 CSResourceGroup17 이라는 컨테이너 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b0889-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="b0889-111">변수</span><span class="sxs-lookup"><span data-stu-id="b0889-111">PARAMETERS</span></span>

### <span data-ttu-id="b0889-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0889-112">-DefaultProfile</span></span>
<span data-ttu-id="b0889-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b0889-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0889-114">-이름</span><span class="sxs-lookup"><span data-stu-id="b0889-114">-Name</span></span>
<span data-ttu-id="b0889-115">이 cmdlet이 가져오는 컨테이너 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0889-115">Specifies the name of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b0889-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0889-116">-ResourceGroupName</span></span>
<span data-ttu-id="b0889-117">이 cmdlet이 가져오는 컨테이너 서비스의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0889-117">Specifies the resource group of the container service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0889-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0889-118">CommonParameters</span></span>
<span data-ttu-id="b0889-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0889-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0889-120">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0889-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0889-121">입력</span><span class="sxs-lookup"><span data-stu-id="b0889-121">INPUTS</span></span>

### <span data-ttu-id="b0889-122">않아야</span><span class="sxs-lookup"><span data-stu-id="b0889-122">None</span></span>
<span data-ttu-id="b0889-123">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0889-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b0889-124">출력</span><span class="sxs-lookup"><span data-stu-id="b0889-124">OUTPUTS</span></span>

### <span data-ttu-id="b0889-125">PSContainerService의. m a.</span><span class="sxs-lookup"><span data-stu-id="b0889-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="b0889-126">상속자</span><span class="sxs-lookup"><span data-stu-id="b0889-126">NOTES</span></span>

## <span data-ttu-id="b0889-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0889-127">RELATED LINKS</span></span>

[<span data-ttu-id="b0889-128">새로운 AzContainerService</span><span class="sxs-lookup"><span data-stu-id="b0889-128">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="b0889-129">제거-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="b0889-129">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="b0889-130">업데이트-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="b0889-130">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


