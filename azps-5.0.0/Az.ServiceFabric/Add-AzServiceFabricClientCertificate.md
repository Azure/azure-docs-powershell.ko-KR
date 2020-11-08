---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
ms.openlocfilehash: ca9dbbba29e6f770b727e1f96717c2626f112839
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216829"
---
# <span data-ttu-id="5671c-101">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="5671c-101">Add-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="5671c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5671c-102">SYNOPSIS</span></span>
<span data-ttu-id="5671c-103">클라이언트 인증을 위해 클러스터에 일반 이름 또는 지문을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5671c-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="5671c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5671c-104">SYNTAX</span></span>

### <span data-ttu-id="5671c-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="5671c-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5671c-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="5671c-106">SingleUpdateWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5671c-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="5671c-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5671c-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="5671c-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5671c-109">설명은</span><span class="sxs-lookup"><span data-stu-id="5671c-109">DESCRIPTION</span></span>
<span data-ttu-id="5671c-110">**AzServiceFabricClientCertificate** 를 사용 하 여 일반 이름 및 발급자 손도장 또는 인증서 지문을 클러스터에 추가 하 여 클라이언트가 인증에 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="5671c-110">Use **Add-AzServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="5671c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="5671c-111">EXAMPLES</span></span>

### <span data-ttu-id="5671c-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="5671c-112">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="5671c-113">이 명령은 지문이 ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A ' 인 인증서를 클러스터에 추가 하므로 클라이언트가 관리자 권한으로이 인증서를 사용 하 여 클러스터와 통신할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5671c-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="5671c-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="5671c-114">Example 2</span></span>
```
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="5671c-115">이 명령은 일반 이름인 읽기 전용 클라이언트 인증서를 추가 합니다. ' Contoso.com '이 고 발급자 손도장은 클러스터에 대 한 ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A '입니다.</span><span class="sxs-lookup"><span data-stu-id="5671c-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="5671c-116">변수</span><span class="sxs-lookup"><span data-stu-id="5671c-116">PARAMETERS</span></span>

### <span data-ttu-id="5671c-117">-관리자</span><span class="sxs-lookup"><span data-stu-id="5671c-117">-Admin</span></span>
<span data-ttu-id="5671c-118">클라이언트 인증 유형</span><span class="sxs-lookup"><span data-stu-id="5671c-118">Client authentication type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SingleUpdateWithThumbprint, SingleUpdateWithCommonName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5671c-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="5671c-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="5671c-120">관리자 권한만 있는 클라이언트 인증서 지문 지정</span><span class="sxs-lookup"><span data-stu-id="5671c-120">Specify client certificate thumbprint which only has admin permission</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5671c-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="5671c-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="5671c-122">클라이언트 일반 이름, 발급자 지문 및 인증 유형 지정</span><span class="sxs-lookup"><span data-stu-id="5671c-122">Specify client common name , issuer thumbprint and authentication type</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]
Parameter Sets: MultipleUpdatesWithCommonName
Aliases: CertCommonName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5671c-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="5671c-123">-CommonName</span></span>
<span data-ttu-id="5671c-124">클라이언트 인증서 일반 이름 지정</span><span class="sxs-lookup"><span data-stu-id="5671c-124">Specify client certificate common name</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5671c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5671c-125">-DefaultProfile</span></span>
<span data-ttu-id="5671c-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5671c-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5671c-127">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="5671c-127">-IssuerThumbprint</span></span>
<span data-ttu-id="5671c-128">클라이언트 인증서 발급자의 지문 지정</span><span class="sxs-lookup"><span data-stu-id="5671c-128">Specify thumbprint of client certificate's issuer</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5671c-129">-이름</span><span class="sxs-lookup"><span data-stu-id="5671c-129">-Name</span></span>
<span data-ttu-id="5671c-130">클러스터 이름 지정</span><span class="sxs-lookup"><span data-stu-id="5671c-130">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="5671c-131">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="5671c-131">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="5671c-132">읽기 전용 권한만 있는 클라이언트 인증서 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5671c-132">Specify client certificate thumbprint which only has read only permission</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5671c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5671c-133">-ResourceGroupName</span></span>
<span data-ttu-id="5671c-134">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5671c-134">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="5671c-135">-지문</span><span class="sxs-lookup"><span data-stu-id="5671c-135">-Thumbprint</span></span>
<span data-ttu-id="5671c-136">클라이언트 인증서 지문 지정</span><span class="sxs-lookup"><span data-stu-id="5671c-136">Specify client certificate thumbprint</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithThumbprint
Aliases: ClientCertificateThumbprint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5671c-137">-확인</span><span class="sxs-lookup"><span data-stu-id="5671c-137">-Confirm</span></span>
<span data-ttu-id="5671c-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5671c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5671c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5671c-139">-WhatIf</span></span>
<span data-ttu-id="5671c-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5671c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5671c-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5671c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5671c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5671c-142">CommonParameters</span></span>
<span data-ttu-id="5671c-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5671c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5671c-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5671c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5671c-145">입력</span><span class="sxs-lookup"><span data-stu-id="5671c-145">INPUTS</span></span>

### <span data-ttu-id="5671c-146">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5671c-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="5671c-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5671c-147">System.String</span></span>

### <span data-ttu-id="5671c-148">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="5671c-148">System.String[]</span></span>

### <span data-ttu-id="5671c-149">ServiceFabric. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="5671c-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="5671c-150">출력</span><span class="sxs-lookup"><span data-stu-id="5671c-150">OUTPUTS</span></span>

### <span data-ttu-id="5671c-151">ServiceFabric 클러스터의 모든.</span><span class="sxs-lookup"><span data-stu-id="5671c-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="5671c-152">상속자</span><span class="sxs-lookup"><span data-stu-id="5671c-152">NOTES</span></span>

## <span data-ttu-id="5671c-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5671c-153">RELATED LINKS</span></span>

[<span data-ttu-id="5671c-154">제거-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="5671c-154">Remove-AzServiceFabricClientCertificate</span></span>](./Remove-AzServiceFabricClientCertificate.md)
