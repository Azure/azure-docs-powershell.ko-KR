---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceVaultSecretGroupObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceVaultSecretGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceVaultSecretGroupObject.md
ms.openlocfilehash: 925d29e7d567613bbf10e88c65860ebe2ef40c2e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200737"
---
# <span data-ttu-id="b81ef-101">New-AzCloudServiceVaultSecretGroupObject</span><span class="sxs-lookup"><span data-stu-id="b81ef-101">New-AzCloudServiceVaultSecretGroupObject</span></span>

## <span data-ttu-id="b81ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b81ef-102">SYNOPSIS</span></span>
<span data-ttu-id="b81ef-103">자격 증명 모음 비밀 그룹에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="b81ef-103">Create a in-memory object for Vault Secret Group</span></span>

## <span data-ttu-id="b81ef-104">구문</span><span class="sxs-lookup"><span data-stu-id="b81ef-104">SYNTAX</span></span>

```
New-AzCloudServiceVaultSecretGroupObject [-CertificateUrl <String[]>] [-Id <String>] [<CommonParameters>]
```

## <span data-ttu-id="b81ef-105">설명</span><span class="sxs-lookup"><span data-stu-id="b81ef-105">DESCRIPTION</span></span>
<span data-ttu-id="b81ef-106">비밀 그룹에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="b81ef-106">Create a in-memory object for Secret Group</span></span>

## <span data-ttu-id="b81ef-107">예제</span><span class="sxs-lookup"><span data-stu-id="b81ef-107">EXAMPLES</span></span>

### <span data-ttu-id="b81ef-108">예제 1: 자격 증명 모음 비밀 그룹 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="b81ef-108">Example 1: Create vault secret group object</span></span>
```powershell
$keyVault = Get-AzKeyVault -VaultName 'ContosoKeyVault'
$certificate = Get-AzKeyVaultCertificate -VaultName 'ContosoKeyVault' -Name 'ContosoCert'
$secretGroup = New-AzCloudServiceVaultSecretGroupObject -Id $keyVault.ResourceId -CertificateUrl $certificate.SecretId
```

<span data-ttu-id="b81ef-109">이 명령은 클라우드 서비스를 만들거나 업데이트하는 데 사용되는 자격 증명 모음 비밀 그룹 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b81ef-109">This command creates vault secret group object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="b81ef-110">자세한 내용은 New-AzCloudService를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="b81ef-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="b81ef-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b81ef-111">PARAMETERS</span></span>

### <span data-ttu-id="b81ef-112">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="b81ef-112">-CertificateUrl</span></span>
<span data-ttu-id="b81ef-113">Key Vault에 비밀로 업로드된 인증서의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="b81ef-113">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b81ef-114">-Id</span><span class="sxs-lookup"><span data-stu-id="b81ef-114">-Id</span></span>
<span data-ttu-id="b81ef-115">Key Vault 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b81ef-115">Key Vault Resource Id.</span></span>

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

### <span data-ttu-id="b81ef-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b81ef-116">CommonParameters</span></span>
<span data-ttu-id="b81ef-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b81ef-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b81ef-118">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b81ef-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b81ef-119">입력</span><span class="sxs-lookup"><span data-stu-id="b81ef-119">INPUTS</span></span>

## <span data-ttu-id="b81ef-120">출력</span><span class="sxs-lookup"><span data-stu-id="b81ef-120">OUTPUTS</span></span>

### <span data-ttu-id="b81ef-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceVaultSecretGroup</span><span class="sxs-lookup"><span data-stu-id="b81ef-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceVaultSecretGroup</span></span>

## <span data-ttu-id="b81ef-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b81ef-122">NOTES</span></span>

<span data-ttu-id="b81ef-123">별칭</span><span class="sxs-lookup"><span data-stu-id="b81ef-123">ALIASES</span></span>

## <span data-ttu-id="b81ef-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b81ef-124">RELATED LINKS</span></span>

