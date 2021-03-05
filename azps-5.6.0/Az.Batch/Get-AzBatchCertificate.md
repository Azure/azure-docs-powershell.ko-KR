---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A9C98F8F-90F2-4BF4-A234-31966FBB975B
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchCertificate.md
ms.openlocfilehash: efbb5cb58342f7b2b6a9be4ab13c4e160fea7c0b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007376"
---
# <span data-ttu-id="c5299-101">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="c5299-101">Get-AzBatchCertificate</span></span>

## <span data-ttu-id="c5299-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5299-102">SYNOPSIS</span></span>
<span data-ttu-id="c5299-103">Batch 계정에서 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c5299-103">Gets the certificates in a Batch account.</span></span>

## <span data-ttu-id="c5299-104">구문</span><span class="sxs-lookup"><span data-stu-id="c5299-104">SYNTAX</span></span>

### <span data-ttu-id="c5299-105">ODataFilter(기본값)</span><span class="sxs-lookup"><span data-stu-id="c5299-105">ODataFilter (Default)</span></span>
```
Get-AzBatchCertificate [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5299-106">지문</span><span class="sxs-lookup"><span data-stu-id="c5299-106">Thumbprint</span></span>
```
Get-AzBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String> [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5299-107">설명</span><span class="sxs-lookup"><span data-stu-id="c5299-107">DESCRIPTION</span></span>
<span data-ttu-id="c5299-108">**Get-AzBatchCertificate** cmdlet은 *BatchContext* 매개 변수가 지정하는 Azure Batch 계정의 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c5299-108">The **Get-AzBatchCertificate** cmdlet gets the certificates in the Azure Batch account that the *BatchContext* parameter specifies.</span></span>
<span data-ttu-id="c5299-109">특정 인증서를 얻습니다. *지문Algorithm* 및 지문 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="c5299-109">To obtain a particular certificate, specify the *ThumbprintAlgorithm* and *Thumbprint* parameters.</span></span>
<span data-ttu-id="c5299-110">필터 *매개* 변수를 지정하여 OData(Open Data Protocol) 필터와 일치하는 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c5299-110">Specify the *Filter* parameter to get the certificates that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="c5299-111">예제</span><span class="sxs-lookup"><span data-stu-id="c5299-111">EXAMPLES</span></span>

### <span data-ttu-id="c5299-112">예제 1: 지문으로 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c5299-112">Example 1: Get a certificate by thumbprint</span></span>
```
PS C:\>Get-AzBatchCertificate -ThumbprintAlgorithm "sha1" - Thumbprint "C1E494A415149C5F211C4778B52F2E834A07247C" -BatchContext $Context
Thumbprint                  : c1e494a415149c5f211c4778b52f2e834a07247c
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=C1E494A415149C5F211C4778B52F2E834A07247
C)
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:16 PM
PreviousState               :
PreviousStateTransitionTime :
Data                        :
CertificateFormat           :
Password                    :
PublicData                  : MIIB9DCCAWGgAwIBAgIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAxMB4XDTE1MTAwMjE2MjkwNVoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDEwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAM06unpRipn3BmHBM75d0s8w/Wwifci16PoJo4c2V68GwsCCFsNOn5
ypo7BBXo1fpBjrnso5w+koaE5LjxkBSVm+TkogwbKlW6WURTM0O5viRVbPnEEU/Y01Pj5cJElFuLEk9Uoe/r/lP8b5A607t1cPjSXkwhEZEYc3LkHDSo0ZAgMBAAGjS
zBJMEcGA1UdAQRAMD6AEFRsTAsrvF+FmPuICooZXaKhGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMYIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAA4GBALt0F8Ep
+8XVE/M2aNtxzlku72gxiOiAo1HmpUaixXx3gl8kdP3xgoKMaq4JskqdLmbJJUnCQ3wmzsdPwjswsW2ycT12zuBddaiS+id98k8U/KYc6FxMgS+H70FYOxARLn7P4FS
SBf/QCyign+BherzezdZ5NBdfzbmWxIMP5iFJ
DeleteCertificateError      :
```

<span data-ttu-id="c5299-113">이 명령은 지정된 지문이 있는 단일 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c5299-113">This command gets a single certificate that has the specified thumbprint.</span></span>
<span data-ttu-id="c5299-114">인증서 지문 알고리즘은 sha1입니다.</span><span class="sxs-lookup"><span data-stu-id="c5299-114">The certificate thumbprint algorithm is sha1.</span></span>

### <span data-ttu-id="c5299-115">예제 2: 필터링된 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c5299-115">Example 2: Get filtered certificates</span></span>
```
PS C:\>Get-AzBatchCertificate -Filter "state eq 'active'" -BatchContext $Context
Thumbprint                  : 025b351b087a084c5067f5e71eff8591970323f9
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=025b351b087a084c5067f5e71eff8591970323f9)
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:17 PM
PreviousState               :
PreviousStateTransitionTime :
Data                        :
CertificateFormat           :
Password                    :
PublicData                  : MIIB9DCCAWGgAwIBAgIQy9W5y8iwhppGhtAG06dHKTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAyMB4XDTE1MTAwMjE2MjkxNFoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDIwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAJxagvVrlnKfv6hfzSiFJUkdGkPjC3tFiKebK6IaeHzesFdFfupXUE
wT0xOWh9xwa3OVkPECEc/u1sw3iVX/J4AODiwzmOWutoVRpWjxGFpgw9+dPvXMjs/Ue7JL7ag3siHs5EcarW91qKbgtko6i/r4emaRyk60U93TrbWQAWJ9AgMBAAGjS
zBJMEcGA1UdAQRAMD6AEAdqsOpyeXF/uDe7ZGKeez+hGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMoIQy9W5y8iwhppGhtAG06dHKTAJBgUrDgMCHQUAA4GBAC0MaAem
6ByyURFvGnFZyjEepjXC5wcaGq+gguDFe8rG88ceig1ZqewdcmC1y4p05uBhbmETbYVWzJarNsHYq2LTihi4t2J4jt2YVYz/IRdUB82iaFFbJRSPrN+6xD3KM2lve5N
4OjtlZAdiXiSUYFf3I6ypberUsAdba3QQajCN
DeleteCertificateError      :

Thumbprint                  : c1e494a415149c5f211c4778b52f2e834a07247c
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=c1e494a415149c5f211c4778b52f2e834a07247c)
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:16 PM
PreviousState               :
PreviousStateTransitionTime :
Data                        :
CertificateFormat           :
Password                    :
PublicData                  : MIIB9DCCAWGgAwIBAgIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAxMB4XDTE1MTAwMjE2MjkwNVoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDEwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAM06unpRipn3BmHBM75d0s8w/Wwifci16PoJo4c2V68GwsCCFsNOn5
ypo7BBXo1fpBjrnso5w+koaE5LjxkBSVm+TkogwbKlW6WURTM0O5viRVbPnEEU/Y01Pj5cJElFuLEk9Uoe/r/lP8b5A607t1cPjSXkwhEZEYc3LkHDSo0ZAgMBAAGjS
zBJMEcGA1UdAQRAMD6AEFRsTAsrvF+FmPuICooZXaKhGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMYIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAA4GBALt0F8Ep
+8XVE/M2aNtxzlku72gxiOiAo1HmpUaixXx3gl8kdP3xgoKMaq4JskqdLmbJJUnCQ3wmzsdPwjswsW2ycT12zuBddaiS+id98k8U/KYc6FxMgS+H70FYOxARLn7P4FS
SBf/QCyign+BherzezdZ5NBdfzbmWxIMP5iFJ
DeleteCertificateError      :
```

<span data-ttu-id="c5299-116">이 명령은 Batch 계정에서 활성 상태의 모든 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c5299-116">This command gets all certificates in the active state from the Batch account.</span></span>
<span data-ttu-id="c5299-117">필터 *매개* 변수는 상태를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c5299-117">The *Filter* parameter specifies the state.</span></span>

## <span data-ttu-id="c5299-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c5299-118">PARAMETERS</span></span>

### <span data-ttu-id="c5299-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c5299-119">-BatchContext</span></span>
<span data-ttu-id="c5299-120">Batch 서비스와 상호 작용하는 데 이 cmdlet이 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c5299-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c5299-121">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻으면 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5299-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c5299-122">대신 공유 키 인증을 사용 Get-AzBatchAccountKey cmdlet을 사용하여 액세스 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c5299-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c5299-123">공유 키 인증을 사용하는 경우 기본 액세스 키는 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5299-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c5299-124">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c5299-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5299-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5299-125">-DefaultProfile</span></span>
<span data-ttu-id="c5299-126">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c5299-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5299-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="c5299-127">-Filter</span></span>
<span data-ttu-id="c5299-128">OData 필터 절을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c5299-128">Specifies an OData filter clause.</span></span>
<span data-ttu-id="c5299-129">이 매개 변수를 지정하면 이 cmdlet은 필터와 일치하는 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c5299-129">If you specify this parameter, this cmdlet gets the certificates that match the filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5299-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="c5299-130">-MaxCount</span></span>
<span data-ttu-id="c5299-131">반환할 인증서의 최대 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c5299-131">Specifies the maximum number of certificates to return.</span></span>
<span data-ttu-id="c5299-132">0(0) 이하의 값을 지정하는 경우 cmdlet은 상한을 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c5299-132">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="c5299-133">기본값은 1000입니다.</span><span class="sxs-lookup"><span data-stu-id="c5299-133">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5299-134">-Select</span><span class="sxs-lookup"><span data-stu-id="c5299-134">-Select</span></span>
<span data-ttu-id="c5299-135">OData select 절을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c5299-135">Specifies an OData select clause.</span></span>
<span data-ttu-id="c5299-136">이 매개 변수에 대한 값을 지정하여 모든 개체 속성이 아닌 특정 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c5299-136">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5299-137">-지문</span><span class="sxs-lookup"><span data-stu-id="c5299-137">-Thumbprint</span></span>
<span data-ttu-id="c5299-138">이 cmdlet이 얻을 인증서의 지문을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c5299-138">Specifies the thumbprint of the certificate that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: Thumbprint
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5299-139">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="c5299-139">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="c5299-140">지문 매개 변수를 파생하는 데 사용되는 *알고리즘을* 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c5299-140">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="c5299-141">현재 유효한 값은 sha1뿐입니다.</span><span class="sxs-lookup"><span data-stu-id="c5299-141">Currently, the only valid value is sha1.</span></span>

```yaml
Type: System.String
Parameter Sets: Thumbprint
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5299-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5299-142">CommonParameters</span></span>
<span data-ttu-id="c5299-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c5299-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5299-144">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5299-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5299-145">입력</span><span class="sxs-lookup"><span data-stu-id="c5299-145">INPUTS</span></span>

### <span data-ttu-id="c5299-146">System.String</span><span class="sxs-lookup"><span data-stu-id="c5299-146">System.String</span></span>

### <span data-ttu-id="c5299-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c5299-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c5299-148">출력</span><span class="sxs-lookup"><span data-stu-id="c5299-148">OUTPUTS</span></span>

### <span data-ttu-id="c5299-149">Microsoft.Azure.Commands.Bat. Models.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="c5299-149">Microsoft.Azure.Commands.Batch.Models.PSCertificate</span></span>

## <span data-ttu-id="c5299-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c5299-150">NOTES</span></span>

## <span data-ttu-id="c5299-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5299-151">RELATED LINKS</span></span>

[<span data-ttu-id="c5299-152">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="c5299-152">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="c5299-153">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="c5299-153">New-AzBatchCertificate</span></span>](./New-AzBatchCertificate.md)

[<span data-ttu-id="c5299-154">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="c5299-154">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="c5299-155">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c5299-155">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
