---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClientCertificate.md
ms.openlocfilehash: c7b6e00ccbe368267fd6b110490df4f70b2229a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532627"
---
# <span data-ttu-id="ac442-101">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ac442-101">Add-AzureRmServiceFabricClientCertificate</span></span>

## <span data-ttu-id="ac442-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac442-102">SYNOPSIS</span></span>
<span data-ttu-id="ac442-103">클라이언트 인증을 위해 클러스터에 일반 이름 또는 지문을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac442-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac442-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ac442-104">SYNTAX</span></span>

### <span data-ttu-id="ac442-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="ac442-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac442-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="ac442-106">SingleUpdateWithCommonName</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac442-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="ac442-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac442-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="ac442-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac442-109">설명은</span><span class="sxs-lookup"><span data-stu-id="ac442-109">DESCRIPTION</span></span>
<span data-ttu-id="ac442-110">**AzureRmServiceFabricClientCertificate** 를 사용 하 여 일반 이름 및 발급자 손도장 또는 인증서 지문을 클러스터에 추가 하 여 클라이언트가 인증에 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac442-110">Use **Add-AzureRmServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="ac442-111">예제의</span><span class="sxs-lookup"><span data-stu-id="ac442-111">EXAMPLES</span></span>

### <span data-ttu-id="ac442-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="ac442-112">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="ac442-113">이 명령은 지문이 ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A ' 인 인증서를 클러스터에 추가 하므로 클라이언트가 관리자 권한으로이 인증서를 사용 하 여 클러스터와 통신할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac442-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="ac442-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="ac442-114">Example 2</span></span>
```
PS c:> Add-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="ac442-115">이 명령은 일반 이름인 읽기 전용 클라이언트 인증서를 추가 합니다. ' Contoso.com '이 고 발급자 손도장은 클러스터에 대 한 ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A '입니다.</span><span class="sxs-lookup"><span data-stu-id="ac442-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="ac442-116">변수</span><span class="sxs-lookup"><span data-stu-id="ac442-116">PARAMETERS</span></span>

### <span data-ttu-id="ac442-117">-관리자</span><span class="sxs-lookup"><span data-stu-id="ac442-117">-Admin</span></span>
<span data-ttu-id="ac442-118">클라이언트 인증 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="ac442-118">Client authentication type.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SingleUpdateWithThumbprint, SingleUpdateWithCommonName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac442-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="ac442-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="ac442-120">관리자 권한만 있는 클라이언트 인증서 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac442-120">Specify client certificate thumbprint that only has admin permission.</span></span>

```yaml
Type: String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac442-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="ac442-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="ac442-122">클라이언트 일반 이름, 발급자 지문, 인증 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac442-122">Specify client common name, issuer thumbprint, and authentication type.</span></span>

```yaml
Type: PSClientCertificateCommonName[]
Parameter Sets: MultipleUpdatesWithCommonName
Aliases: CertCommonName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac442-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="ac442-123">-CommonName</span></span>
<span data-ttu-id="ac442-124">클라이언트 인증서 일반 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac442-124">Specify client certificate common name.</span></span>

```yaml
Type: String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac442-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac442-125">-DefaultProfile</span></span>
<span data-ttu-id="ac442-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ac442-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac442-127">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="ac442-127">-IssuerThumbprint</span></span>
<span data-ttu-id="ac442-128">클라이언트 인증서 발급자 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac442-128">Specify client certificate issuer thumbprint.</span></span>

```yaml
Type: String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac442-129">-이름</span><span class="sxs-lookup"><span data-stu-id="ac442-129">-Name</span></span>
<span data-ttu-id="ac442-130">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac442-130">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac442-131">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="ac442-131">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="ac442-132">읽기 전용 권한이 있는 클라이언트 인증서 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac442-132">Specify client certificate thumbprint that has read only permission.</span></span>

```yaml
Type: String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac442-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac442-133">-ResourceGroupName</span></span>
<span data-ttu-id="ac442-134">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac442-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ac442-135">-지문</span><span class="sxs-lookup"><span data-stu-id="ac442-135">-Thumbprint</span></span>
<span data-ttu-id="ac442-136">클라이언트 인증서 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac442-136">Specify client certificate thumbprint.</span></span>

```yaml
Type: String
Parameter Sets: SingleUpdateWithThumbprint
Aliases: ClientCertificateThumbprint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac442-137">-확인</span><span class="sxs-lookup"><span data-stu-id="ac442-137">-Confirm</span></span>
<span data-ttu-id="ac442-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac442-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac442-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac442-139">-WhatIf</span></span>
<span data-ttu-id="ac442-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ac442-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac442-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ac442-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac442-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac442-142">CommonParameters</span></span>
<span data-ttu-id="ac442-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac442-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac442-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac442-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac442-145">입력</span><span class="sxs-lookup"><span data-stu-id="ac442-145">INPUTS</span></span>

### <span data-ttu-id="ac442-146">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="ac442-146">System.Collections.Hashtable</span></span>
<span data-ttu-id="ac442-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ac442-147">System.String</span></span>

<span data-ttu-id="ac442-148">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="ac442-148">System.Boolean</span></span>

## <span data-ttu-id="ac442-149">출력</span><span class="sxs-lookup"><span data-stu-id="ac442-149">OUTPUTS</span></span>

### <span data-ttu-id="ac442-150">ServiceFabric 클러스터의 모든.</span><span class="sxs-lookup"><span data-stu-id="ac442-150">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="ac442-151">상속자</span><span class="sxs-lookup"><span data-stu-id="ac442-151">NOTES</span></span>

## <span data-ttu-id="ac442-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ac442-152">RELATED LINKS</span></span>

[<span data-ttu-id="ac442-153">제거-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ac442-153">Remove-AzureRmServiceFabricClientCertificate</span></span>](./Remove-AzureRmServiceFabricClientCertificate.md)
