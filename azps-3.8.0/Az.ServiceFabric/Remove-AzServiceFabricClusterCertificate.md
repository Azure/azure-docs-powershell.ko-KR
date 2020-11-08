---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: 3d5f3ce0e941d8359087db792cdf3c8a721bba39
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041710"
---
# <span data-ttu-id="d4a7a-101">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="d4a7a-101">Remove-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="d4a7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4a7a-102">SYNOPSIS</span></span>
<span data-ttu-id="d4a7a-103">클러스터 보안에 사용 되지 않도록 클러스터 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4a7a-103">Remove a cluster certificate from being used for cluster security.</span></span>

## <span data-ttu-id="d4a7a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d4a7a-104">SYNTAX</span></span>

```
Remove-AzServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4a7a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d4a7a-105">DESCRIPTION</span></span>
<span data-ttu-id="d4a7a-106">클러스터에서 이미 사용 중인 다른 유효한 인증서가 있는 경우 **remove-AzServiceFabricClusterCertificate** 를 사용 하 여 클러스터에서 클러스터 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4a7a-106">Use **Remove-AzServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="d4a7a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d4a7a-107">EXAMPLES</span></span>

### <span data-ttu-id="d4a7a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d4a7a-108">Example 1</span></span>
```
PS C:\> Remove-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="d4a7a-109">이 명령은 클러스터 보안에 사용할 지문이 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A 인 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4a7a-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="d4a7a-110">변수</span><span class="sxs-lookup"><span data-stu-id="d4a7a-110">PARAMETERS</span></span>

### <span data-ttu-id="d4a7a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4a7a-111">-DefaultProfile</span></span>
<span data-ttu-id="d4a7a-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d4a7a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4a7a-113">-이름</span><span class="sxs-lookup"><span data-stu-id="d4a7a-113">-Name</span></span>
<span data-ttu-id="d4a7a-114">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4a7a-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="d4a7a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4a7a-115">-ResourceGroupName</span></span>
<span data-ttu-id="d4a7a-116">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4a7a-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d4a7a-117">-지문</span><span class="sxs-lookup"><span data-stu-id="d4a7a-117">-Thumbprint</span></span>
<span data-ttu-id="d4a7a-118">제거할 클러스터 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4a7a-118">Specify the cluster thumbprint which to be removed.</span></span>

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

### <span data-ttu-id="d4a7a-119">-확인</span><span class="sxs-lookup"><span data-stu-id="d4a7a-119">-Confirm</span></span>
<span data-ttu-id="d4a7a-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4a7a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4a7a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4a7a-121">-WhatIf</span></span>
<span data-ttu-id="d4a7a-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d4a7a-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4a7a-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d4a7a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4a7a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4a7a-124">CommonParameters</span></span>
<span data-ttu-id="d4a7a-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4a7a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4a7a-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4a7a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4a7a-127">입력</span><span class="sxs-lookup"><span data-stu-id="d4a7a-127">INPUTS</span></span>

### <span data-ttu-id="d4a7a-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d4a7a-128">System.String</span></span>

## <span data-ttu-id="d4a7a-129">출력</span><span class="sxs-lookup"><span data-stu-id="d4a7a-129">OUTPUTS</span></span>

### <span data-ttu-id="d4a7a-130">ServiceFabric 클러스터의 모든.</span><span class="sxs-lookup"><span data-stu-id="d4a7a-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="d4a7a-131">상속자</span><span class="sxs-lookup"><span data-stu-id="d4a7a-131">NOTES</span></span>

## <span data-ttu-id="d4a7a-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d4a7a-132">RELATED LINKS</span></span>
