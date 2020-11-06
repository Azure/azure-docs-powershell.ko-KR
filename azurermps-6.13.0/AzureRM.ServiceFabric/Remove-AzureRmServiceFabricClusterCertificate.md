---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClusterCertificate.md
ms.openlocfilehash: 088f90af1ce80bdda390de1ce62a9d38581344aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530061"
---
# <span data-ttu-id="c9332-101">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="c9332-101">Remove-AzureRmServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="c9332-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9332-102">SYNOPSIS</span></span>
<span data-ttu-id="c9332-103">클러스터 보안에 사용 되지 않도록 클러스터 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9332-103">Remove a cluster certificate from being used for cluster security.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9332-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c9332-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9332-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c9332-105">DESCRIPTION</span></span>
<span data-ttu-id="c9332-106">클러스터에서 이미 사용 중인 다른 유효한 인증서가 있는 경우 **remove-AzureRmServiceFabricClusterCertificate** 를 사용 하 여 클러스터에서 클러스터 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9332-106">Use **Remove-AzureRmServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="c9332-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c9332-107">EXAMPLES</span></span>

### <span data-ttu-id="c9332-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c9332-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="c9332-109">이 명령은 클러스터 보안에 사용할 지문이 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A 인 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9332-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="c9332-110">변수</span><span class="sxs-lookup"><span data-stu-id="c9332-110">PARAMETERS</span></span>

### <span data-ttu-id="c9332-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9332-111">-DefaultProfile</span></span>
<span data-ttu-id="c9332-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c9332-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9332-113">-이름</span><span class="sxs-lookup"><span data-stu-id="c9332-113">-Name</span></span>
<span data-ttu-id="c9332-114">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9332-114">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9332-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9332-115">-ResourceGroupName</span></span>
<span data-ttu-id="c9332-116">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9332-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c9332-117">-지문</span><span class="sxs-lookup"><span data-stu-id="c9332-117">-Thumbprint</span></span>
<span data-ttu-id="c9332-118">제거할 클러스터 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9332-118">Specify the cluster thumbprint which to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9332-119">-확인</span><span class="sxs-lookup"><span data-stu-id="c9332-119">-Confirm</span></span>
<span data-ttu-id="c9332-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9332-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9332-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9332-121">-WhatIf</span></span>
<span data-ttu-id="c9332-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c9332-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9332-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9332-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9332-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9332-124">CommonParameters</span></span>
<span data-ttu-id="c9332-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9332-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9332-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9332-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9332-127">입력</span><span class="sxs-lookup"><span data-stu-id="c9332-127">INPUTS</span></span>

### <span data-ttu-id="c9332-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c9332-128">System.String</span></span>
<span data-ttu-id="c9332-129">매개 변수: 지문 (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c9332-129">Parameters: Thumbprint (ByValue)</span></span>

## <span data-ttu-id="c9332-130">출력</span><span class="sxs-lookup"><span data-stu-id="c9332-130">OUTPUTS</span></span>

### <span data-ttu-id="c9332-131">ServiceFabric 클러스터의 모든.</span><span class="sxs-lookup"><span data-stu-id="c9332-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="c9332-132">상속자</span><span class="sxs-lookup"><span data-stu-id="c9332-132">NOTES</span></span>

## <span data-ttu-id="c9332-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9332-133">RELATED LINKS</span></span>
