---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationAzureActiveDirectoryApp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
ms.openlocfilehash: 8eec47c703290047b51ce38e97391500a9f27d74
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194617"
---
# <span data-ttu-id="cce77-101">New-AzDataMigrationAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="cce77-101">New-AzDataMigrationAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="cce77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cce77-102">SYNOPSIS</span></span>
<span data-ttu-id="cce77-103">새 인스턴스 DataMigration Azure ActiveDirectory 애플리케이션 세부 정보를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="cce77-103">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="cce77-104">구문</span><span class="sxs-lookup"><span data-stu-id="cce77-104">SYNTAX</span></span>

```
New-AzDataMigrationAzureActiveDirectoryApp -ApplicationId <String> -AppKey <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cce77-105">설명</span><span class="sxs-lookup"><span data-stu-id="cce77-105">DESCRIPTION</span></span>
<span data-ttu-id="cce77-106">새 인스턴스 DataMigration Azure ActiveDirectory 애플리케이션 세부 정보를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="cce77-106">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="cce77-107">예제</span><span class="sxs-lookup"><span data-stu-id="cce77-107">EXAMPLES</span></span>

### <span data-ttu-id="cce77-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="cce77-108">Example 1</span></span>
```powershell
PS C:\> $secpasswd = ConvertTo-SecureString "Your Secret Key Here" -AsPlainText -Force
C:\> New-AzDmsAadApp -ApplicationId "Your AppId/Service Principal ID here" -AppKey $secpasswd
```
<span data-ttu-id="cce77-109">ApplicationId: "AppId/Service Principal Id here" AppKey : System.Security.SecureString TenantId : "Tenant ID"</span><span class="sxs-lookup"><span data-stu-id="cce77-109">ApplicationId : "Your AppId/Service Principal Id here" AppKey        : System.Security.SecureString TenantId      : "Tenant Id"</span></span>

## <span data-ttu-id="cce77-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cce77-110">PARAMETERS</span></span>

### <span data-ttu-id="cce77-111">-AppKey</span><span class="sxs-lookup"><span data-stu-id="cce77-111">-AppKey</span></span>
<span data-ttu-id="cce77-112">Azure Active Directory 키</span><span class="sxs-lookup"><span data-stu-id="cce77-112">Azure Active Directory Key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: Key

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cce77-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="cce77-113">-ApplicationId</span></span>
<span data-ttu-id="cce77-114">Azure Active Directory 애플리케이션 ID</span><span class="sxs-lookup"><span data-stu-id="cce77-114">Azure Active Directory Application Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cce77-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cce77-115">-DefaultProfile</span></span>
<span data-ttu-id="cce77-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cce77-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cce77-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cce77-117">CommonParameters</span></span>
<span data-ttu-id="cce77-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cce77-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="cce77-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cce77-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cce77-120">입력</span><span class="sxs-lookup"><span data-stu-id="cce77-120">INPUTS</span></span>

### <span data-ttu-id="cce77-121">없음</span><span class="sxs-lookup"><span data-stu-id="cce77-121">None</span></span>

## <span data-ttu-id="cce77-122">출력</span><span class="sxs-lookup"><span data-stu-id="cce77-122">OUTPUTS</span></span>

### <span data-ttu-id="cce77-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="cce77-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="cce77-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cce77-124">NOTES</span></span>

## <span data-ttu-id="cce77-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cce77-125">RELATED LINKS</span></span>
