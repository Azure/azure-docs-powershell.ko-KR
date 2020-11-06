---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 0093393f926af257e07b7d697a7f267fa62b483a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525820"
---
# <span data-ttu-id="0e1bf-101">New-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="0e1bf-101">New-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="0e1bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e1bf-102">SYNOPSIS</span></span>
<span data-ttu-id="0e1bf-103">새 Analysis Services 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0e1bf-103">Creates a new Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e1bf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0e1bf-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesServer [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e1bf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0e1bf-105">DESCRIPTION</span></span>
<span data-ttu-id="0e1bf-106">New-AzureRmAnalysisServicesServer cmdlet은 새 Analysis Services 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0e1bf-106">The New-AzureRmAnalysisServicesServer cmdlet creates a new Analysis Services server</span></span>

## <span data-ttu-id="0e1bf-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0e1bf-107">EXAMPLES</span></span>

### <span data-ttu-id="0e1bf-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0e1bf-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesServer -ResourceGroupName "testresourcegroup" -Name "testserver" -Location "West-US" -Sku "S1"
```

<span data-ttu-id="0e1bf-109">Azure 지역 서 비 US 및 리소스 그룹 testresrourcegroup에서 testserver 라는 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0e1bf-109">Creates a server named testserver in the Azure region West-US and in resource group testresrourcegroup.</span></span> <span data-ttu-id="0e1bf-110">서버에 대 한 sku 수준은 S1이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e1bf-110">The sku level for the server will be S1.</span></span>

## <span data-ttu-id="0e1bf-111">변수</span><span class="sxs-lookup"><span data-stu-id="0e1bf-111">PARAMETERS</span></span>

### <span data-ttu-id="0e1bf-112">-관리자</span><span class="sxs-lookup"><span data-stu-id="0e1bf-112">-Administrator</span></span>
<span data-ttu-id="0e1bf-113">서버의 관리자로 설정할 사용자 또는 그룹의 쉼표로 구분 된 목록을 나타내는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="0e1bf-113">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span> <span data-ttu-id="0e1bf-114">사용자 또는 그룹에 UPN 형식 (예: 또는)을 지정 해야 합니다. user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="0e1bf-114">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e1bf-115">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="0e1bf-115">-BackupBlobContainerUri</span></span>
<span data-ttu-id="0e1bf-116">Analysis Services 서버 백업용 blob 컨테이너 Uri</span><span class="sxs-lookup"><span data-stu-id="0e1bf-116">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e1bf-117">-위치</span><span class="sxs-lookup"><span data-stu-id="0e1bf-117">-Location</span></span>
<span data-ttu-id="0e1bf-118">Analysis Services 서버가 호스팅되는 Azure 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="0e1bf-118">The Azure region where the Analysis Services server is hosted</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: North Central US, South Central US, Central US, West Europe, North Europe, West US, East US, East US 2, Japan East, Japan West, Brazil South, Southeast Asia, East Asia, Australia East, Australia Southeast

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e1bf-119">-이름</span><span class="sxs-lookup"><span data-stu-id="0e1bf-119">-Name</span></span>
<span data-ttu-id="0e1bf-120">Analysis Services 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e1bf-120">Name of the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e1bf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e1bf-121">-ResourceGroupName</span></span>
<span data-ttu-id="0e1bf-122">서버가 속한 Azure 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="0e1bf-122">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="0e1bf-123">-Sku</span><span class="sxs-lookup"><span data-stu-id="0e1bf-123">-Sku</span></span>
<span data-ttu-id="0e1bf-124">서버의 Sku 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e1bf-124">The name of the Sku for the server.</span></span>
<span data-ttu-id="0e1bf-125">지원 되는 값은 표준 계층에 대 한 0 ', ' 1 ', ' 2 ', 4 '입니다. 기본 계층에 대 한 ' B1 ', ' B2 ', 개발 계층의 경우 1 '입니다.</span><span class="sxs-lookup"><span data-stu-id="0e1bf-125">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e1bf-126">태그</span><span class="sxs-lookup"><span data-stu-id="0e1bf-126">-Tag</span></span>
<span data-ttu-id="0e1bf-127">서버에서 태그로 설정 된 해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="0e1bf-127">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e1bf-128">-확인</span><span class="sxs-lookup"><span data-stu-id="0e1bf-128">-Confirm</span></span>
<span data-ttu-id="0e1bf-129">사용자에 게 작업 수행 여부 확인 메시지 표시</span><span class="sxs-lookup"><span data-stu-id="0e1bf-129">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e1bf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e1bf-130">-WhatIf</span></span>
<span data-ttu-id="0e1bf-131">현재 작업이 실제로 수행 하지 않고 수행 하는 작업에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e1bf-131">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e1bf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e1bf-132">CommonParameters</span></span>
<span data-ttu-id="0e1bf-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e1bf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e1bf-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e1bf-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e1bf-135">입력</span><span class="sxs-lookup"><span data-stu-id="0e1bf-135">INPUTS</span></span>

## <span data-ttu-id="0e1bf-136">출력</span><span class="sxs-lookup"><span data-stu-id="0e1bf-136">OUTPUTS</span></span>

### <span data-ttu-id="0e1bf-137">AnalysisServices. AzureAnalysisServicesServer/.</span><span class="sxs-lookup"><span data-stu-id="0e1bf-137">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="0e1bf-138">상속자</span><span class="sxs-lookup"><span data-stu-id="0e1bf-138">NOTES</span></span>
<span data-ttu-id="0e1bf-139">별칭: New-AzureAs</span><span class="sxs-lookup"><span data-stu-id="0e1bf-139">Alias: New-AzureAs</span></span>

## <span data-ttu-id="0e1bf-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e1bf-140">RELATED LINKS</span></span>

[<span data-ttu-id="0e1bf-141">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="0e1bf-141">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="0e1bf-142">제거-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="0e1bf-142">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
