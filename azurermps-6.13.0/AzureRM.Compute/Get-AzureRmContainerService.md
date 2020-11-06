---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmContainerService.md
ms.openlocfilehash: 0f87254f72d0b5ac22a5770ad3f1a9d03b70fd34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528612"
---
# <span data-ttu-id="ee153-101">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="ee153-101">Get-AzureRmContainerService</span></span>

## <span data-ttu-id="ee153-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee153-102">SYNOPSIS</span></span>
<span data-ttu-id="ee153-103">컨테이너 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ee153-103">Gets a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee153-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ee153-104">SYNTAX</span></span>

```
Get-AzureRmContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee153-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ee153-105">DESCRIPTION</span></span>
<span data-ttu-id="ee153-106">**Get-AzureRmContainerService** cmdlet은 컨테이너 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ee153-106">The **Get-AzureRmContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="ee153-107">상태, 마스터 및 에이전트 수, 마스터 및 에이전트의 정규화 된 도메인 이름 등 컨테이너 서비스의 속성을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ee153-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="ee153-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ee153-108">EXAMPLES</span></span>

### <span data-ttu-id="ee153-109">예제 1: 컨테이너 서비스 가져오기</span><span class="sxs-lookup"><span data-stu-id="ee153-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="ee153-110">이 명령은 CSResourceGroup17 이라는 컨테이너 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ee153-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="ee153-111">변수</span><span class="sxs-lookup"><span data-stu-id="ee153-111">PARAMETERS</span></span>

### <span data-ttu-id="ee153-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee153-112">-DefaultProfile</span></span>
<span data-ttu-id="ee153-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ee153-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee153-114">-이름</span><span class="sxs-lookup"><span data-stu-id="ee153-114">-Name</span></span>
<span data-ttu-id="ee153-115">이 cmdlet이 가져오는 컨테이너 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee153-115">Specifies the name of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee153-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee153-116">-ResourceGroupName</span></span>
<span data-ttu-id="ee153-117">이 cmdlet이 가져오는 컨테이너 서비스의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee153-117">Specifies the resource group of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee153-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee153-118">CommonParameters</span></span>
<span data-ttu-id="ee153-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee153-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee153-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee153-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee153-121">입력</span><span class="sxs-lookup"><span data-stu-id="ee153-121">INPUTS</span></span>

### <span data-ttu-id="ee153-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ee153-122">System.String</span></span>

## <span data-ttu-id="ee153-123">출력</span><span class="sxs-lookup"><span data-stu-id="ee153-123">OUTPUTS</span></span>

### <span data-ttu-id="ee153-124">PSContainerService의. m a.</span><span class="sxs-lookup"><span data-stu-id="ee153-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="ee153-125">상속자</span><span class="sxs-lookup"><span data-stu-id="ee153-125">NOTES</span></span>

## <span data-ttu-id="ee153-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee153-126">RELATED LINKS</span></span>

[<span data-ttu-id="ee153-127">새로운 AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="ee153-127">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="ee153-128">제거-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="ee153-128">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="ee153-129">업데이트-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="ee153-129">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


